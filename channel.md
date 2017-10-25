# channel
Functions to query and manipulate the list of channels.

A TVH user can only see via the API those channels to which access has been allowed. However a user with ADMIN privilege can use the parameter `all=1` to see details of every channel, channeltag and category even if they do not have access to them.

## channel/class
Lists the text strings, options and defaults used when configuring channels within TVH (ie Configuration -> Channel/EPG -> Channel -> Add). It is only likely to be needed for recreating the existing TVH GUI.
## channel/grid
Lists details of channels. For details of the parameters and selection criteria which can be applied, see [Grid Parameters](Description.md#grid-parameters).
```
{
   "entries" : [
      {
         "dvr_pst_time" : 0,
         "enabled" : true,
         "epgauto" : true,
         "autoname" : true,
         "name" : "BBC RB 1",
         "number" : 601,
         "tags" : [
            "21d5fe751062c4d99997d6cb48f43c55",
            "1a2a61c4374cedb1fc29417f1a517446"
         ],
         "services" : [
            "9b0e2e103a373350f5e99cda6dd3f055"
         ],
         "epg_running" : -1,
         "epggrab" : [],
         "uuid" : "ae63d3b40fbfab610f49290abc189472",
         "bouquet" : "",
         "dvr_pre_time" : 0
      }, ...
   ],
   "total" : 104
}
```
## channel/list
Lists the names and uuids of all known channels.
```
{
   "entries" : [
      {
         "val" : "Channel 5+1",
         "key" : "7e7b77801531c803f5ce8f4d5003f44c"
      }, ...
   ]
}
```
## channel/create
Creates a new channel.

- `conf` A JSON object containing details of the new channel.
## channeltag/class
Lists the text strings, options and defaults used when configuring channels within TVH (ie Configuration -> Channel/EPG -> Channel Tags -> Add). It is only likely to be needed for recreating the existing TVH GUI.
## channeltag/grid
Lists details of channel tags. For details of the parameters and selection criteria which can be applied, see [Grid Parameters](Description.md#grid-parameters).
```
{
   "total" : 5,
   "entries" : [
      {
         "index" : 0,
         "private" : false,
         "icon_public_url" : "",
         "internal" : false,
         "name" : "Radio",
         "titled_icon" : false,
         "enabled" : true,
         "uuid" : "3479ac5a48d6680fc37d8b411cf0e2e8",
         "icon" : "",
         "comment" : ""
      }, ...
   ]
}
```
## channeltag/list
Lists the names and uuids of all channel tags.
```
{
   "entries" : [
      {
         "key" : "3479ac5a48d6680fc37d8b411cf0e2e8",
         "val" : "Radio"
      }, ...
   ]
}
```
## channeltag/create
Creates a new channel tag.

- `conf` A JSON object containing details of the new channel tag.
## channelcategory/list
??
