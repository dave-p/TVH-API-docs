# API Description
TVHeadend provides the API using the HTTP protocol, by default via port 9981 though this can be changed in the TVH config. Both the GET and POST methods may be used.

The URL must include a username and password with access permissions to carry out the requested task. If TVHeadend has been started with the '--http_root' qualifier, the HTTP root must be included in the URL, thus eg

`http://admin:admin@192.168.3.45:9981/myHttpRoot/api/config/capabilities`

The response from TVH follows the HTTP protocol and includes a status indicating successful completion or the nature of any error.

Data is usually returned as JSON, without any CR or LF characters - the examples given have been 'prettified' to make them easier to read. Functions which perform an action rather than return data will return an empty JSON object on successful completion.

## Grid parameters
API calls which end in `/grid`, with the exception of `epg/event/grid`, have a common set of parameters:
- `start` First entry to include. Default is the first.
- `limit` Number of entries to include. **Default is 50** - use a large number to get all.
- `filter` A JSON object describing the filter(s) to be applied. See [Grid Filters](Description.md#grid-filters) below for syntax.
- `sort` Name of the field to sort the records by. A case-sensitive sort is used.
- `dir` if `sort` is specified then `dir=desc` produces a reverse sort.
### Grid filters
A filter can be applied to the output using a JSON object. The syntax is:
```
filter=[
            {
                "field" : "<fieldname>"
                "type"  : "string|numeric|boolean"
                "value" : "<value>"
                "comparison" : "gt|lt|eq"
             }, ...
        ]
```
The "comparison" field is only used with numeric data; booleans must match exactly while for strings a regular expression match is used.
## Code examples
### curl
Parameters passed to TVH using the GET method must be URI-encoded:

`curl 'http://user:pass@localhost:9981/api/epg/events/grid?limit=999&channel=BBC%20ONE'`

Alternatively use the POST Method:

`curl --data 'limit=999&channel=BBC ONE' 'http://user:pass@localhost:9981/api/epg/events/grid'`

To make the output more human-readable, pipe it through json_pp (included in the perl package on many distributions).
### PHP
This simple example lists some details about upcoming timers, sorted in date order. To work through a PHP-enabled web server, the PHP.INI setting "allow_url_fopen" must be ON.
```
$timers = get_timers();
foreach($timers as $t) {
    $start = strftime("%H:%M", $t["start"]);
    $stop = strftime("%H:%M", $t["stop"]);
    $date = strftime("%a %e/%m", $t["start"]);
    echo "Date: $date, Start: $start, End: $stop, Title: {$t['disp_title']}";
}

function get_timers() {
  $url = "http://admin:admin@localhost:9981/api/dvr/entry/grid_upcoming?sort=start";
  $json = file_get_contents($url);
  $j = json_decode($json, true);
  $ret = &$j["entries"];
  return $ret;
}
```
