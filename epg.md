# epg
Functions to query the Electronic Program(me) Guide.
## epg/events/grid
Query the EPG and optionally apply filters. Parameters are:
- `lang` ?
- `mode` If set to the string `now` then only events currently playing are listed.
- `title` A string which must appear in the title to be listed.
- `fulltext` If set to 1 then the `title` string must match exactly. Default is 0.
- `channel` Name of the channel to show events from.
- `channelTag` ?
- `durationMin` Shortest event to be listed.
- `durationMax` Longest event to be listed.
- `contentType` Integer representing the genre to be listed (where from?).
- `filter` ??
- `sort` ??
- `start` First record to be listed, default is 0.
- `limit` Number of records to list. **Default is 50**.
```
{
   "totalCount" : 18575,
   "entries" : [
      {
         "widescreen" : 1,
         "episodeId" : 905306,
         "start" : 1508893500,
         "summary" : "Love Run Cold: Danny, Flack, and Lindsay encounter a rapidly-melting crime scene when a model is found dead at an ice-themed promotional party for vodka, apparently stabbed by an icicle. (S3 ...[AD,S]",
         "channelNumber" : "56",
         "serieslinkId" : 900760,
         "stop" : 1508897100,
         "subtitle" : "Love Run Cold: Danny, Flack, and Lindsay encounter a rapidly-melting crime scene when a model is found dead at an ice-themed promotional party for vodka, apparently stabbed by an icicle. (S3 ...[AD,S]",
         "episodeUri" : "crid://www.five.tv/V3V34",
         "subtitled" : 1,
         "channelUuid" : "c764464e95df34cff2cb37ce1c3eafe7",
         "audiodesc" : 1,
         "channelName" : "5USA+1",
         "serieslinkUri" : "crid://www.five.tv/R38IU",
         "eventId" : 905390,
         "nextEventId" : 905391,
         "title" : "CSI: New York"
      }
   ]
}
```

## epg/events/alternative

## epg/events/related

## epg/events/load

## epg/brand/list

## epg/content_type/list
