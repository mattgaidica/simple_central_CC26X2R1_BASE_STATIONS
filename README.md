##Functions##
_BTN1 (Left)_: Reset `curTime` and `nvsOffset`. Turns on LEDR until next `BASE_TIME_INTERVAL`.

_BTN2 (Right)_: Export data. Turns on both LEDs while executing `ESLO_EXPORT_DATA` and turns them off at the end.

_Time Found_: Enqueues `ESLO_TIME_FOUND`.

_Log Advertisement_: `ESLO_LogAdvertisement` is called when a bio-logger is recognized.

_Increment Time Event_: Adds `BASE_TIME_INTERVAL` (1000ms) to `curTime`.

##Set Time Details##
See [Reading time from peripheral to update central](https://e2e.ti.com/support/wireless-connectivity/bluetooth-group/bluetooth/f/bluetooth-forum/1025080/cc2652r-reading-time-from-peripheral-to-update-central)

1. The time is set in `SimpleCentral_processGATTMsg()` by `pMsg->msg.readRsp.pValue`.
2. 