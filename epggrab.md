# epggrab

## epggrab/channel/list
TODO
## epggrab/channel/class
Lists the parameters, descriptions, options and defaults for the GUI screen Configuration -> Channel/EPG -> EPG Grabber Channels.
## epggrab/channel/grid
TODO
## epggrab/module/list
List EPG Grabber Modules, as shown in the GUI screen Configuration -> Channel/EPG -> EPG Grabber Modules.
```
{
   "entries" : [
      {
         "uuid" : "13ba822c654b492183fbd462cd2700f6",
         "title" : "External: XMLTV",
         "status" : "epggrabmodNone"
      }, ...
   ]
}
```
## epggrab/config/load
TODO
## epggrab/config/save
TODO
## epggrab/ota/trigger
Queues a run of the OTA EPG grabber.
- `trigger` Delay in seconds before the run starts. Minimum is one second, maximum is one week.
## epggrab/internal/rerun
Run the internal EPG grabbers immediately.
- `rerun` Not used but must be an integer greater than zero.
