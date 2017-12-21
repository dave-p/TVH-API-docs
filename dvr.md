# DVR
This section includes functions to manipulate recorder objects; timers, autorecs and recordings.

## dvr/config/class
Lists the text strings, options and defaults used when configuring the DVR capability within TVH (ie Configuration -> Recording). 
## dvr/config/grid
Lists the configuration sets available for the TVH server together with their options. Configurations are identified by their `name` parameter; the default config has the name blank.
```
{
   "total" : 1,
   "entries" : [
      {
         "cache" : 2,
         "storage-mfree" : 1000,
         "autorec-maxsched" : 0,
         "whitespace-in-title" : false,
         "time-in-title" : false,
         "channel-dir" : false,
         "epg-running" : true,
         "name" : "",
         "episode-in-title" : false,
         "profile" : "af143f0983fd4e91953fb859c5561984",
         "clean-title" : false,
         "pre-extra-time" : 0,
         "uuid" : "4e3a1e1cacd2d559c129e7b90f6c986e",
         "day-dir" : false,
         "subtitle-in-title" : false,
         "epg-update-window" : 86400,
         "title-dir" : false,
         "warm-time" : 30,
         "windows-compatible-filenames" : false,
         "autorec-maxcount" : 0,
         "removal-days" : 2147483647,
         "storage-mused" : 0,
         "tag-files" : true,
         "clone" : true,
         "omit-title" : false,
         "enabled" : true,
         "storage" : "/mnt/tvheadend",
         "date-in-title" : false,
         "channel-in-title" : false,
         "post-extra-time" : 0,
         "skip-commercials" : false,
         "rerecord-errors" : 0,
         "file-permissions" : "0664",
         "retention-days" : 2147483646,
         "charset" : "ASCII",
         "pri" : 2,
         "directory-permissions" : "0775",
         "pathname" : "$t$n.$x"
      }
   ]
}
```
## dvr/config/create
Creates a new configuration set. Parameters passed are:
- `name` configuration name
- `conf` parameter set, passed as a JSON object
## dvr/entry/class
Lists the text strings, options and defaults used when editing an upcoming recording.

## dvr/entry/grid
Lists all of the recordings that TVH knows about, ie it combines the output of `grid_upcoming`, `grid_finished`, `grid_failed` and `grid_removed`. Use the `status` parameter to tell them apart.

See [Grid Parameters](Description.md#grid-parameters) for parameter details.
## dvr/entry/grid_upcoming
Lists all of the currently-scheduled recordings. See [Grid Parameters](Description.md#grid-parameters) for parameter details.
```
{
   "total" : 6,
   "entries" : [
      {
         "comment" : "Auto recording: Created from EPG query",
         "creator" : "xxxxxx",
         "disp_description" : "Documentary series. A driver raises the alarm when he suspects that his train has hit something on the line, and engineers begin the process of dismantling a Victorian viaduct. (S1 Ep 6)[S]",
         "start_extra" : 0,
         "noresched" : false,
         "stop_extra" : 0,
         "enabled" : true,
         "description" : {
            "eng" : "Documentary series. A driver raises the alarm when he suspects that his train has hit something on the line, and engineers begin the process of dismantling a Victorian viaduct. (S1 Ep 6)[S]"
         },
         "title" : {
            "eng" : "Paddington Station 24/7"
         },
         "subtitle" : {
            "eng" : "Documentary series. A driver raises the alarm when he suspects that his train has hit something on the line, and engineers begin the process of dismantling a Victorian viaduct. (S1 Ep 6)[S]"
         },
         "start_real" : 1508724570,
         "duplicate" : 0,
         "removal" : 0,
         "dvb_eid" : 29271,
         "channel_icon" : "",
         "start" : 1508724600,
         "channelname" : "Channel 5 HD",
         "autorec" : "f2c30b9757e66567bf2d8ec6de60314c",
         "config_name" : "4e3a1e13acd2d5a9c129e7b00f6c986e",
         "timerec" : "",
         "stop_real" : 1508727600,
         "content_type" : 8,
         "parent" : "",
         "disp_subtitle" : "Documentary series. A driver raises the alarm when he suspects that his train has hit something on the line, and engineers begin the process of dismantling a Victorian viaduct. (S1 Ep 6)[S]",
         "filename" : "",
         "errorcode" : 0,
         "duration" : 3000,
         "timerec_caption" : "",
         "child" : "",
         "errors" : 0,
         "playcount" : 0,
         "norerecord" : false,
         "url" : "",
         "playposition" : 0,
         "data_errors" : 0,
         "stop" : 1508727600,
         "sched_status" : "scheduled",
         "broadcast" : 898373,
         "status" : "Scheduled for recording",
         "disp_title" : "Paddington Station 24/7",
         "filesize" : 0,
         "pri" : 6,
         "channel" : "a931256950c3f8aa5c5416cd36175e13",
         "uuid" : "52f0c81843b3f87ee276bdd02c325d52",
         "fileremoved" : 0,
         "autorec_caption" : " (Created from EPG query)",
         "owner" : "xxxxxx",
         "retention" : 0
      } ...
 ]
}
```
## dvr/entry/grid_finished
Lists recordings which have completed and which are still in the TVH logs. See [Grid Parameters](Description.md#grid-parameters) for parameter details.
```
{
   "total" : 37,
   "entries" : [
      {
         "enabled" : true,
         "disp_subtitle" : "It's Spring and Dick buys a tractor, with plans to tame the walled garden. Angel designs a new boudoir with black walls and mirrors. The couple also consider truffle farming. (S3 Ep2/3)  [AD,S]",
         "channel_icon" : "",
         "errorcode" : 0,
         "config_name" : "4e3a1e13acd2d5a9c129e7b00f6c986e",
         "broadcast" : 0,
         "owner" : "xxxxxx",
         "noresched" : true,
         "stop_real" : 1506884400,
         "filename" : "/video/tvheadend/Escape to the Chateau-1.ts",
         "playposition" : 0,
         "start_real" : 1506880770,
         "duration" : 3600,
         "removal" : 0,
         "disp_description" : "It's Spring and Dick buys a tractor, with plans to tame the walled garden. Angel designs a new boudoir with black walls and mirrors. The couple also consider truffle farming. (S3 Ep2/3)  [AD,S]",
         "status" : "Completed OK",
         "subtitle" : {
           "eng" : "It's Spring and Dick buys a tractor, with plans to tame the walled garden. Angel designs a new boudoir with black walls and mirrors. The couple also consider truffle farming. (S3 Ep2/3)  [AD,S]"
        },
        "autorec_caption" : "",
        "title" : {
           "eng" : "Escape to the Chateau"
        },
        "autorec" : "",
        "sched_status" : "completed",
        "duplicate" : 0,
        "norerecord" : false,
        "channelname" : "Channel 4 HD",
        "stop_extra" : 0,
        "pri" : 6,
        "channel" : "d6727549be8e6a532ff322c389eb3bd4",
        "errors" : 0,
        "content_type" : 9,
        "timerec" : "",
        "url" : "dvrfile/7b43663e74e11d9a3efda4bf7baa3548",
        "disp_title" : "Escape to the Chateau",
        "filesize" : 2338180064,
        "retention" : 0,
        "description" : {
          "eng" : "It's Spring and Dick buys a tractor, with plans to tame the walled garden. Angel designs a new boudoir with black walls and mirrors. The couple also consider truffle farming. (S3 Ep2/3)  [AD,S]"
       },
       "stop" : 1506884400,
       "child" : "",
       "comment" : "Auto recording: Created from EPG query",
       "playcount" : 0,
       "start" : 1506880800,
       "data_errors" : 0,
       "parent" : "",
       "start_extra" : 0,
       "uuid" : "7b4366de74e11d9a3ef0a4bf7baa3548",
       "timerec_caption" : "",
       "fileremoved" : 0,
       "dvb_eid" : 0,
       "creator" : "xxxxxx"
    } ...
    ]
 }
```
## dvr/entry/grid_failed
Lists failed recordings. See [Grid Parameters](Description.md#grid-parameters) for parameter details.

If you merge the 'failed' and 'completed' recordings into a single list, the only way to tell which list the entries originally came from is by using the `status` field.
```{
   "total" : 1,
   "entries" : [
      {
         "parent" : "",
         "channelname" : "BBC Four HD",
         "start" : 1513112400,
         "stop_real" : 1513116000,
         "description" : {
            "eng" : "2/3. Series in which Sam Willis reveals stories of invasion in Britain, including the Barbary Corsaire pirates and the tale of King Louis the Lion, who invaded in the 13th century. [HD] [S]"
         },
         "comment" : "Auto recording: Created from EPG query",
         "disp_title" : "New: Invasion! with Sam Willis",
         "child" : "",
         "uri" : "crid://fp.bbc.co.uk/247LP4",
         "image" : "",
         "dvb_eid" : 62795,
         "autorec_caption" : " (Created from EPG query)",
         "removal" : 0,
         "url" : "dvrfile/22d9847b550b8fe9e39e01bda2e41777",
         "owner" : "xxxxxx",
         "copyright_year" : 0,
         "playposition" : 0,
         "filename" : "/video/tvheadend/New: Invasion! with Sam Willis.ts",
         "start_real" : 1513112355,
         "start_extra" : 0,
         "duration" : 3600,
         "category" : [],
         "creator" : "xxxxxx",
         "playcount" : 0,
         "sched_status" : "completed",
         "status" : "Too many data errors",
         "autorec" : "5cf012bf5c78e23d3c89c59c172414cb",
         "errors" : 0,
         "norerecord" : false,
         "broadcast" : 0,
         "noresched" : true,
         "keyword" : [],
         "config_name" : "ffb7136480e16dac47c8e71bd7686537",
         "disp_subtitle" : "2/3. Series in which Sam Willis reveals stories of invasion in Britain, including the Barbary Corsaire pirates and the tale of King Louis the Lion, who invaded in the 13th century. [HD] [S]",
         "enabled" : true,
         "stop_extra" : 0,
         "pri" : 6,
         "retention" : 0,
         "subtitle" : {
            "eng" : "2/3. Series in which Sam Willis reveals stories of invasion in Britain, including the Barbary Corsaire pirates and the tale of King Louis the Lion, who invaded in the 13th century. [HD] [S]"
         },
         "disp_description" : "2/3. Series in which Sam Willis reveals stories of invasion in Britain, including the Barbary Corsaire pirates and the tale of King Louis the Lion, who invaded in the 13th century. [HD] [S]",
         "fileremoved" : 0,
         "filesize" : 2171129092,
         "credits" : {},
         "title" : {
            "eng" : "New: Invasion! with Sam Willis"
         },
         "content_type" : 2,
         "genre" : [],
         "errorcode" : 0,
         "stop" : 1513116000,
         "channel_icon" : "",
         "data_errors" : 510410,
         "timerec" : "",
         "channel" : "7bd448424af369b19f22511b1ece023c",
         "uuid" : "22d9847b550b8fe9e39e01bda2e41777",
         "timerec_caption" : "",
         "first_aired" : 0,
         "duplicate" : 0
      }
   ]
}
```
## dvr/entry/grid_removed
Lists removed recordings. See [Grid Parameters](Description.md#grid-parameters) for parameter details.

If TVH is configured to delete the log record when a recording is deleted this function will always return nothing.
## dvr/entry/create
Creates a new epg-derived timer from a JSON object.

- `conf` The JSON object describing the timer. Items not specified are derived from the default profile of the user. An example of the minimum useful JSON is shown below.
```
{
   "start":1509397200,
   "stop":1509400800,
   "channelname":"Channel 5",
   "title":{
      "eng":"Paddington Station 24/7"
   },
   "subtitle":{"eng":"More real-life dramas..."}
}
```
The function returns the uuid of the created timer on success.

It is also possible using this function to add a file created elsewhere into the TVH database as a completed recording. Items needed in the JSON are:
```
{
    "enabled": true,
    "start": 1509000000,
    "stop":  1509003600,
    "channelname": "local file",
    "title": {
        "eng": "my title" 
    },
    "subtitle": {
        "eng": "filename: my video" 
    },
    "description": {
        "eng": "my description" 
    },
    "comment": "added by tvh_addfile.py",
    "files": [
        {
            "filename": "/full/path/to/videofile.ts" 
        }
    ]
}
```
It is important that the start and stop times are in the past, otherwise TVH will try to create a timer to record the event. *(Thanks to "ullix tv" for this information.)* Also note that the ability to add a pre-recorded file is unintended behaviour - see [Caution](Intro.md#caution).
## dvr/entry/create_by_event
Creates a new one-off timer. Input parameters are:
- `config_uuid` this is the `uuid` parameter from the output of `dvr/config/grid`
- `event_id` this is the `eventId` parameter for the event, taken from `epg/events/grid`
## dvr/entry/rerecord/toggle
Set the recording to be re-done if not already set, or cancel a rerecording if one was scheduled. This is the same fuction as Digital Video Recorder -> Finished Recordings -> Re-record.
- `uuid` the `uuid` of the finished or failed recording, or a JSON object containing an array of uuids.
## dvr/entry/rerecord/deny
Cancel a planned re-recording. See **dvr/entry/rerecord/toggle** above.
## dvr/entry/rerecord/allow
Schedule a re-recording. See **dvr/entry/rerecord/toggle** above.
## dvr/entry/stop
Gracefully stops a running recording.
- `uuid` The `uuid` value from the timer's entry in `dvr/entry/grid`.
## dvr/entry/cancel
Deletes a timer or stops a running recording.
- `uuid` The `uuid` value from the timer's entry in `dvr/entry/grid`.

**NOTE** To delete a series use `idnode/delete`, passing parameter `uuid` from the entry in `dvr/timerec/grid`.
## dvr/entry/prevrec/toggle, dvr/entry/prevrec/set, dvr/entry/prevrec/unset
These three functions affect the "previously recorded" status of a timer. If set, either directly or via a call to the toggle function, the timer is marked as completed and the file flagged as deleted. If unset, a new timer is created.

These functions can be used to 'hide' re-runs to prevent them being re-recorded.
## dvr/entry/remove
Removes a completed recording from storage.
- `uuid` The recording's `uuid` value from `dvr/entry/grid_finished`.
## dvr/entry/filemoved
Informs TVH that a recording has been relocated (by external means) within the filesystem.
- `src` The original full path to the file
- `dst` The new full path to the file
## dvr/entry/move/finished
Move a **finished** recording entry to the "Finished Recordings" category, presumably from "Failed Recordings". The actual file is not moved.
- `uuid` The `uuid` of the entry, or an array of entries passed as a JSON object.
## dvr/entry/move/failed
Move a **finished** recording entry to the "Failed Recordings" category, presumably from "Finished Recordings". The actual file is not moved.
- `uuid` The `uuid` of the entry, or an array of entries passed as a JSON object.
## dvr/autorec/class
Lists the text strings, options and defaults used when creating or editing a series timer.
## dvr/autorec/grid
Lists autorecs (series timers). See [Grid Parameters](Description.md#grid-parameters) for parameter details.
```
{
   "entries" : [
      {
         "record" : 0,
         "pri" : 6,
         "channel" : "a931256950c3f8aa5c5416cd36175e13",
         "content_type" : 0,
         "retention" : 0,
         "fulltext" : false,
         "start_window" : "Any",
         "serieslink" : "crid://www.five.tv/R5HP0",
         "config_name" : "4e3a1e13acd2d5a9c129e7b00f6c986e",
         "maxduration" : 0,
         "removal" : 0,
         "start_extra" : 0,
         "stop_extra" : 0,
         "maxcount" : 0,
         "owner" : "xxxxxx",
         "weekdays" : [
            1,
            2,
            3,
            4,
            5,
            6,
            7
         ],
         "uuid" : "f2c30b9757e66567bf2d8ec6de60314c",
         "creator" : "xxxxxx",
         "tag" : "",
         "maxsched" : 0,
         "comment" : "Created from EPG query",
         "start" : "Any",
         "btype" : 0,
         "brand" : "",
         "enabled" : true,
         "season" : "",
         "minduration" : 0,
         "title" : "New: Paddington Station 24/7"
      }, ...
   ],
   "total" : 9
}
```
## dvr/autorec/create
Create a new series timer by specifying search parameters. To create a timer using CRIDs use `dvr/autorec/create_by_series`.
- `conf` A JSON object specifying the selection parameters for the timer.
- `config_uuid` The `uuid` parameter from the output of `dvr/config/grid`. Parameter `config_name` may be passed instead.
## dvr/autorec/create_by_series
Creates a new series timer using CRIDs. Input parameters are:
- `config_uuid` The `uuid` parameter from the output of `dvr/config/grid`
- `event_id` The `eventId` parameter for one event in the series, taken from `epg/events/grid`

**NOTE** To delete a series use `idnode/delete`, passing parameter `uuid` from the entry in `dvr/timerec/grid`.
## dvr/timerec/class
Lists the text strings, options and defaults used when creating or editing a time-based recording.
## dvr/timerec/grid
Lists time-based recordings. See [Grid Parameters](Description.md#grid-parameters) for parameter details.
## dvr/timerec/create
Create a new time-based timer.
- `conf` A JSON object specifying the selection parameters for the timer.
