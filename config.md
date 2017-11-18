# config

## config/capabilities
(Purpose unknown.)
```[
   "caclient",
   "tvadapters",
   "imagecache",
   "timeshift",
   "trace",
   "libav"
]
```
## config/load
TODO
## config/save
TODO
## tvhlog/config/load
TODO
## tvhlog/config/save
TODO
## memoryinfo/class
Lists the details and descriptions of items in the TVH GUI screen Configuration -> Debugging -> Memory Information Entries.
## memoryinfo/grid
Lists details of in-memory objects. See [Grid Parameters](Description.md#grid-parameters) for details of selection parameters.
```
{
   "entries" : [
      {
         "peak_count" : 17154,
         "name" : "EPG Broadcasts",
         "uuid" : "a1af1bc4f29ba28104e71a540465f250",
         "count" : 17154,
         "peak_size" : 6235792,
         "size" : 6235792
      },
      {
         "peak_count" : 3285,
         "peak_size" : 369303,
         "count" : 3285,
         "size" : 369303,
         "name" : "EPG Series Links",
         "uuid" : "823a78a3bcd05b688c59871455da6399"
      },
      {
         "count" : 11514,
         "peak_size" : 5015593,
         "size" : 5015593,
         "name" : "EPG Episodes",
         "uuid" : "5c666eea1ec3de4bbb9a11f60116b258",
         "peak_count" : 11514
      }, ...
   ],
   "total" : 19
}
```
