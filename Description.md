# API Description
TVHeadend provides the API using the HTTP protocol, by default via port 9981 though this can be changed in the TVH config. The GET method is used, with parameters passed on the URL.

The URL must include a username and password with access permissions to carry out the requested task. If TVHeadend has been started with the '--http_root' qualifier, the HTTP root must be included in the URL, thus eg

`http://admin:admin@192.168.3.45:9981/myHttpRoot/api/config/capabilities`

The response from TVH follows the HTTP protocol and includes a status indicating successful completion or the nature of any error.

Data is usually returned as JSON, without any CR or LF characters - the examples given have been 'prettified' to make them easier to read. Functions which perform an action rather than return data will return an empty JSON object on successful completion.
## Code examples
### curl
Parameters passed to TVH in the URL must be URI-encoded.
`curl 'http://user:pass@localhost:9981/api/epg/events/grid?limit=999&channel=BBC%20ONE'`
If `http_root` has been set for the server, its value must be included in the URL before the /api.
### PHP
This simple example lists some details about upcoming timers, sorted in date order. To work through a PHP-enabled web server, the PHP.INI setting "allow_url_fopen" must be ON.
```
$urlp = 'http://admin:admin@localhost:9981;'

$timers = get_timers();
foreach($timers as $t) {
    $start = strftime("%H:%M", $t["start"]);
    $stop = strftime("%H:%M", $t["stop"]);
    $date = strftime("%a %e/%m", $t["start"]);
    echo "Date: $date, Start: $start, End: $stop, Title: {$t['disp_title']}";
}

function get_timers() {
  global $urlp;
  $url = "$urlp/api/dvr/entry/grid_upcoming?sort=start";
  $json = file_get_contents($url);
  $j = json_decode($json, true);
  $ret = &$j["entries"];
  return $ret;
}
```
