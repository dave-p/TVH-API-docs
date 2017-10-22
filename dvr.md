# DVR
This section includes functions to manipulate recorder objects; timers, autorecs and recordings.

## dvr/config/class
Lists the text strings, options and defaults used when configuring the DVR capability within TVH (ie Configuration -> Recording). It is only likely to be needed for recreating the existing TVH GUI.
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
- configuration name
- parameter set.

The structure of the parameter set is TBD.
## dvr/entry/class
Lists the text strings, options and defaults used when editing an upcoming recording. It is only likely to be needed for recreating the existing TVH GUI.

## dvr/entry/grid
Lists all of the recordings that TVH knows about, ie it combines the output of `grid_upcoming`, `grid_finished`, `grid_failed` and `grid_removed`. Use the `status` parameter to tell them apart.
## dvr/entry/grid_upcoming
Lists all of the currently-scheduled recordings.
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
Lists recordings which have completed and which are still in the TVH logs.
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
Lists failed recordings?
## dvr/entry/grid_removed
Lists removed recordings?
## dvr/entry/create
???
## dvr/entry/create_by_event
Creates a new one-off timer. Input parameters are:
- `config_uuid` this is the `uuid` parameter from the output of `dvr/config/grid`
- `event_id` this is the `eventId` parameter for the event, taken from `epg/events/grid`
## dvr/entry/rerecord/toggle

## dvr/entry/rerecord/deny

## dvr/entry/rerecord/allow

## dvr/entry/stop

## dvr/entry/cancel

## dvr/entry/remove

## dvr/entry/filemoved

## dvr/entry/move/finished

## dvr/entry/move/failed

## dvr/autorec/class

## dvr/autorec/grid

## dvr/autorec/create

## dvr/autorec/create_by_series

## dvr/timerec/class

## dvr/timerec/grid

## dvr/timerec/create
