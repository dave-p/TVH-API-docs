# status
Lists statistics of input sources and connections.
## status/connections

## status/subscriptions

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
## connections/cancel
