# status
Lists statistics of input sources and connections.
## status/connections
Lists currently-connected client devices.
```
{
   "totalCount" : 1,
   "entries" : [
      {
         "id" : 1,
         "started" : 1508668447,
         "server_port" : 9982,
         "server" : "x.x.x.x",
         "type" : "HTSP",
         "peer" : "x.x.x.y",
         "user" : "xxxxxx",
         "peer_port" : 57496
      }
   ]
}
```
## status/subscriptions
Lists currently-active subscriptions.
```
{
   "entries" : [
      {
         "errors" : 0,
         "title" : "epggrab",
         "in" : 85222,
         "total_in" : 25162474,
         "total_out" : 25162474,
         "id" : 75,
         "out" : 85222,
         "service" : "Silicon Labs Si2168 : DVB-T #0/Sandy/690MHz/Raw PID Subscription",
         "state" : "Running",
         "start" : 1508763840
      }
   ],
   "totalCount" : 1
}
```
## status/inputs
Lists statistics of input devices.

For DVB-T tuners at least, the signal and SNR values are only non-zero while TVH is actively using the device. 
```
{
   "totalCount" : 1,
   "entries" : [
      {
         "snr" : 0,
         "input" : "Siano Mobile Digital MDTV Receiver #0 : DVB-T #0",
         "snr_scale" : 0,
         "tc_block" : 0,
         "ec_block" : 0,
         "signal" : 0,
         "signal_scale" : 0,
         "te" : 0,
         "tc_bit" : 0,
         "ber" : 0,
         "cc" : 0,
         "subs" : 0,
         "weight" : 0,
         "unc" : 0,
         "bps" : 0,
         "uuid" : "2700b3116072cf41e59b13bf77d29781",
         "ec_bit" : 0
      }
   ]
}
```
The meaning of the statistics is below. Not all input sources provide all of the values.
```
subs     => Subscribers
weight   => Weight
bps      => Bandwidth (bits/second)
ber      => Bit Error Rate
unc      => Uncorrected Blocks
te       => Transport Errors
cc       => Continuity Errors
signal   => Signal Strength (dBm)
snr      => Signal/Noise Ratio (dB0
stream   => Stream
ec_block => Block Error Count
tc_bit   => Total Bit Error Count
tc_block => Total Block Error Count
ec_bit   => Bit Error Count
```
## status/inputclrstats
Resets the input counters to zero.
- `uuid` Not clear what this refers to. More than one uuid can be specified.
## connections/cancel
Disconnects one or more clients.
- `id` ids of the connections, obtained from status/connections. How are multiple connections specified??
