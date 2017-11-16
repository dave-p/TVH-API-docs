# bouquet

## bouquet/list
Lists names and bouquets. The list excerpted below is coded into tvheadend.
```
{
   "entries" : [
      {
         "key" : "e7ddb611669a6a612846415946272f89",
         "val" : "Canal Digitaal SD"
      }, ...
   ]
}
```
## bouquet/class
Lists the text strings, options and defaults used when configuring bouquets within TVH (ie Configuration -> Channel/EPG -> Bouquets). It is only likely to be needed for recreating the existing TVH GUI.
## bouquet/grid
Lists details of bouquets. For details of the parameters and selection criteria which can be applied, see [Grid Parameters](Description.md#grid-parameters).
```
{
   "entries" : [
      {
         "name" : "Canal Digitaal SD",
         "uuid" : "e7ddb611669a6a612846415946272f89",
         "lcn_off" : 0,
         "services" : {},
         "chtag_ref" : "",
         "maptoch" : false,
         "source" : "dvb-fastscan://DVB-S,19.2E,12515000,H,22000000,900",
         "ext_url_period" : 60,
         "chtag" : [],
         "services_count" : 0,
         "services_seen" : 0,
         "ssl_peer_verify" : false,
         "mapopt" : [
            "encrypted"
         ],
         "enabled" : false
      }, ...
   ]
   "total" : 13
}
```
## bouquet/create
    
## bouquet/scan
Scan one or more bouquets to find their channels.

- `uuid` uuid(s) of bouquet(s) to scan.
## bouquet/detach
