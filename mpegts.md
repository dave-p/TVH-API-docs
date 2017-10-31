# mpegts

## mpegts/input/network_list

## mpegts/network/grid
Lists available networks. The standard parameters listed in [Grid Parameters](Description.md#grid-parameters) may be used.
```
{
   "entries" : [
      {
         "localtime" : 0,
         "num_mux" : 9,
         "wizard" : false,
         "ignore_chnum" : false,
         "num_svc" : 145,
         "autodiscovery" : 2,
         "skipinitscan" : false,
         "bouquet" : false,
         "sid_chnum" : false,
         "scanq_length" : 0,
         "networkname" : "Sandy",
         "uuid" : "c70bb0e55db15cf44c72a8acb49d5ed7",
         "charset" : "AUTO",
         "pnetworkname" : "",
         "num_chn" : 105,
         "nid" : 0,
         "idlescan" : false
      }
   ],
   "total" : 1
}
```
## mpegts/network/class
Lists the text strings, options and defaults used when configuring the DVB capability within TVH (ie Configuration -> DVB Inputs -> Networks). It is only likely to be needed for recreating the existing TVH GUI.
## mpegts/network/builders
Lists the text strings, options and defaults used when configuring the DVB capability within TVH (ie Configuration -> DVB Inputs -> Network -> Add). It is only likely to be needed for recreating the existing TVH GUI.
## mpegts/network/create

## mpegts/network/mux_class

## mpegts/network/mux_create

## mpegts/network/scan
Triggers a scan of the requested network(s).
- `uuid` uuid(s) of the network(s) to scan. More than one may be given; they will be scanned in sequence.
## mpegts/mux/grid
Lists available multiplexes. The standard parameters listed in [Grid Parameters](Description.md#grid-parameters) may be used.
- `hidemode` If set to `all`, only enabled multiplexes are listed. The default is to show all multiplexes.
```
{
   "total" : 9,
   "entries" : [
      {
         "created" : 1508497835,
         "delsys" : "DVB-T",
         "scan_state" : 0,
         "tsid" : 24640,
         "scan_first" : 1508761027,
         "name" : "690MHz",
         "pnetwork_name" : "Cambs & Beds",
         "transmission_mode" : "8k",
         "sid_filter" : 0,
         "network_uuid" : "c70bb0e55db15cf44c72a8acb49d5ed7",
         "onid" : 9018,
         "num_svc" : 35,
         "eit_tsid_nocheck" : false,
         "num_chn" : 29,
         "hierarchy" : "NONE",
         "tsid_zero" : false,
         "pmt_06_ac3" : 0,
         "network" : "Sandy",
         "scan_last" : 1509267382,
         "bandwidth" : "8MHz",
         "fec_lo" : "NONE",
         "frequency" : 690000000,
         "constellation" : "QAM/64",
         "fec_hi" : "3/4",
         "epg" : 1,
         "guard_interval" : "1/32",
         "scan_result" : 1,
         "enabled" : 1,
         "uuid" : "0245c791efc3fa448c19db2f000d0d8f",
         "plp_id" : -1
      }, ...
   ]
}
```
## mpegts/mux/class
Lists the text strings, options and defaults used when configuring the DVB capability within TVH (ie Configuration -> DVB Inputs -> Muxes). It is only likely to be needed for recreating the existing TVH GUI.
## mpegts/service/grid
Lists available mpegts services. The standard parameters listed in [Grid Parameters](Description.md#grid-parameters) may be used.
- `hidemode` The default is to show only services where the multiplex is enabled and the service has been verified. Setting this parameter to `all` also hides services which are not enabled, setting it to `none` shows all services.
```
{
   "total" : 137,
   "entries" : [
      {
         "prefcapid_lock" : 0,
         "s_type_user" : -1,
         "prefcapid" : 0,
         "lcn_minor" : 0,
         "lcn2" : 0,
         "uuid" : "c5206e5a69625ee60c1c3d23e56b6d22",
         "lcn" : 698,
         "auto" : 0,
         "svcname" : "698",
         "dvb_servicetype" : 1,
         "created" : 1499259842,
         "force_caid" : 0,
         "enabled" : true,
         "channel" : [],
         "priority" : 0,
         "pts_shift" : 0,
         "last_seen" : 1509329042,
         "multiplex_uuid" : "0245c791efc3fa448c19db2f000d0d8f",
         "encrypted" : false,
         "caid" : "",
         "srcid" : 0,
         "dvb_ignore_eit" : false,
         "multiplex" : "690MHz",
         "sid" : 28520,
         "network" : "Sandy"
      }, ...
   ]
}
```
## mpegts/service/class
Lists the text strings, options and defaults used when configuring the DVB capability within TVH (ie Configuration -> DVB Inputs -> Services). It is only likely to be needed for recreating the existing TVH GUI.
## mpegts/mux_sched/class
Lists the text strings, options and defaults used when configuring the DVB capability within TVH (ie Configuration -> DVB Inputs -> Mux Schedulers). It is only likely to be needed for recreating the existing TVH GUI.
## mpegts/mux_sched/grid

## mpegts/mux_sched/create

## dvb/orbitalpos/list
Lists orbital positions and the satellites occupying them. The list is distributed with tvheadend; satellite reception is not necessary to use this API.
```
{
   "entries" : [
      {
         "key" : "177W",
         "val" : "177W : NSS 9"
      }, ...
   ]
}
```
## dvb/scanfile/list
