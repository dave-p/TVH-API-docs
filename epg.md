# epg
Functions to query the Electronic Program(me) Guide.
## epg/events/grid
Query the EPG and optionally apply filters.
- `lang` ?
- `mode` If set to the string `now` then only events currently playing are listed.
- `title` A string which must appear in the title to be listed.
- `fulltext` If set to 1 then the `title` string must match exactly. Default is 0.
- `channel` The channel to show events from, specified either by channel name or uuid. Must be an exact match to the data from `channel/list`, otherwise all channels are returned.
- `channelTag` ?
- `durationMin` Shortest event to be listed (seconds).
- `durationMax` Longest event to be listed (seconds).
- `contentType` Integer representing the genre to be listed - see `epg/content_type/list`.
- `filter` A JSON object describing the filter(s) to be applied. See [Grid Filters](Description.md#grid-filters) for the syntax.
- `sort` The key to be sorted by. Default is to sort by 'start'.
- `dir` If `sort` is specified, setting 'dir' to 'desc' reverses the sort order  
- `start` First record to be listed from the database, default is 0.
- `limit` Number of records to list. **Default is 50** - use a very large number to get all.
- `new` If set to 1 then only events marked as 'new' will be included. Default is 0. The EPG source must identify 'new' events for this filter to work.

EPG sources differ in the information which they provide. Any items which have no data available will be omitted.

```
{
   "totalCount" : 18575,
   "entries" : [
      {
         "serieslinkUri" : "crid://www.channel4.com/M4EI0021031162146302",
         "serieslinkId" : 510179,
         "episodeId" : 510180,
         "episodeUri" : "crid://www.channel4.com/41408/013",
         "summary" : "Tony Robinson and the Team descend on the bleak landscape of Bodmin Moor to examine a Bronze Age village and a vast, ancient 300m-long stone structure.  [S]",
         "genre" : [
            160
         ],
         "channelName" : "More 4",
         "title" : "Time Team",
         "start" : 1508760600,
         "subtitled" : 1,
         "channelUuid" : "e1b1de65605dc4e13bac6d4478e66a44",
         "eventId" : 510178,
         "nextEventId" : 510181,
         "widescreen" : 1,
         "stop" : 1508764500,
         "subtitle" : "Tony Robinson and the Team descend on the bleak landscape of Bodmin Moor to examine a Bronze Age village and a vast, ancient 300m-long stone structure.  [S]",
         "channelNumber" : "14"
      }, ...
   ]
}
```

## epg/events/alternative
Lists alternative broadcasts of the same event.
- `eventId` Identifier of the event, eg taken from `epg/events/grid`.
The function appears to rely on the EPG provider giving details such as episode number. It does not work on UK DVB-T.

This function does not work on TVH versions older than 4.2.4-5 or 4.3-589.
## epg/events/related
Lists alternative broadcasts of the same event.
- `eventId` Identifier of the event, eg taken from `epg/events/grid`.
The function appears to rely on the EPG provider giving details such as episode number. It does not work on UK DVB-T.

This function does not work on TVH versions older than 4.2.4-5 or 4.3-589.
## epg/events/load
Lists details of specific event(s).
- `eventId` Identifier of the event, or a JSON array of event Ids.
```
{
   "entries" : [
      {
         "serieslinkId" : 261067,
         "channelUuid" : "e61af00ea8b71683b9a1f41515fa83d3",
         "title" : "Take Me Out",
         "nextEventId" : 262992,
         "widescreen" : 1,
         "summary" : "Paddy McGuinness presents the dating show. The likely lads include a chocolate factory worker, a city slicker, an oil rig engineer and a gymnast. [S]",
         "channelNumber" : "113",
         "channelName" : "ITV2+1",
         "serieslinkUri" : "crid://www.itv.com/ebs44033",
         "genre" : [
            48
         ],
         "subtitle" : "Paddy McGuinness presents the dating show. The likely lads include a chocolate factory worker, a city slicker, an oil rig engineer and a gymnast. [S]",
         "episodeId" : 262718,
         "episodeUri" : "crid://www.itv.com/1616462450",
         "eventId" : 262991,
         "start" : 1515005400,
         "stop" : 1515009600,
         "subtitled" : 1
      }
   ],
   "totalCount" : 1
}

```
## epg/brand/list
A 'Brand' is a commonly-available show, eg "Eastenders". What constitutes a 'Brand' is up to the EPG provider.
## epg/content_type/list
Lists the Content Type IDs extracted from ETSI EN 300 468 together with their descriptions. The Content Type ID appears in the output of `epg/grid` as "Genre". IDs described as 'Reserved' or 'User Defined' in the specification are given the description of the previous ID instead.
- `full` If set to 0 (the default) only the broad categories defined by `content_nibble_level_1` in the specification are listed. If set to 1 all categories are listed.

```
{
   "entries" : [
      {
         "val" : "",
         "key" : 0
      },
      {
         "val" : "Movie / Drama",
         "key" : 16
      },
      {
         "key" : 17,
         "val" : "Detective / Thriller"
      }, ...
   ]
}
```
