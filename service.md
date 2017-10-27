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

## service/removeunseen
Remove services which have not been seen recently. This call carries out the same action as Configuration -> DVB Inputs -> Services -> Maintenance in the TVH GUI.
- `days` The number of unseen days before deletion. The default is 7 days, the minimum is 5 days.
- `type` If set to `pat` the action is the same as "Remove unseen services (PAT/SDT)" in the GUI. Otherwise the action is the same as "Remove all unseen services".

An empty JSON object is always returned.
