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
## status/inputclrstats

## connections/cancel
