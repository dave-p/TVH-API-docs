# service
## service/mapper/load

## service/mapper/save

## service/mapper/stop
Stops a running service mapper operation.
## service/mapper/status
Provides the same output as Status -> Service Mapper in the TVH GUI.
```
{
   "ignore" : 0,
   "ok" : 0,
   "fail" : 0,
   "total" : 0
}
```
## service/list
Lists available services.
- `enum` If set to 1 (as an integer without quotes) a short-form list is output containing each service's uuid and name. If set to 0 (the default) a verbose list is generated.
- `list` If `enum` is not 1 this parameter selects which items are to be output (details to follow).
## service/streams
Lists the streams comprising the service.
- `uuid` uuid of the service. This parameter is mandatory; it is not possible to list all services.
```
{
   "streams" : [
      {
         "pid" : 1101,
         "type" : "PCR"
      },
      {
         "pid" : 1100,
         "type" : "PMT"
      },
      {
         "aspect_num" : 0,
         "index" : 1,
         "pid" : 1101,
         "type" : "MPEG2VIDEO",
         "aspect_den" : 0,
         "width" : 0,
         "language" : "",
         "height" : 0,
         "duration" : 0
      },
      {
         "audio_type" : 0,
         "type" : "MPEG2AUDIO",
         "audio_version" : 2,
         "language" : "eng",
         "index" : 2,
         "pid" : 1102
      },
      {
         "language" : "eng",
         "audio_version" : 2,
         "index" : 3,
         "pid" : 1103,
         "type" : "MPEG2AUDIO",
         "audio_type" : 3
      },
      {
         "index" : 4,
         "language" : "eng",
         "pid" : 1131,
         "ancillary_id" : 2,
         "type" : "DVBSUB",
         "composition_id" : 2
      }
   ],
   "name" : "Sandy/498MHz/Channel 4",
   "fstreams" : [
      {
         "pid" : 1101,
         "index" : 1,
         "aspect_num" : 0,
         "width" : 0,
         "aspect_den" : 0,
         "type" : "MPEG2VIDEO",
         "height" : 0,
         "language" : "",
         "duration" : 0
      },
      {
         "audio_type" : 0,
         "type" : "MPEG2AUDIO",
         "language" : "eng",
         "audio_version" : 2,
         "index" : 2,
         "pid" : 1102
      },
      {
         "type" : "MPEG2AUDIO",
         "audio_type" : 3,
         "pid" : 1103,
         "audio_version" : 2,
         "language" : "eng",
         "index" : 3
      },
      {
         "language" : "eng",
         "pid" : 1131,
         "index" : 4,
         "ancillary_id" : 2,
         "type" : "DVBSUB",
         "composition_id" : 2
      }
   ]
}
```
## service/removeunseen
Remove services which have not been seen recently. This call carries out the same action as Configuration -> DVB Inputs -> Services -> Maintenance in the TVH GUI.
- `days` The number of unseen days before deletion. The default is 7 days, the minimum is 5 days.
- `type` If set to `pat` the action is the same as "Remove unseen services (PAT/SDT)" in the GUI. Otherwise the action is the same as "Remove all unseen services".

An empty JSON object is always returned.
