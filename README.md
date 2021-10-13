##Functions##
_BTN1 (Left)_: Reset `curTime` and `nvsOffset`. Turns on LEDR until next `BASE_TIME_INTERVAL`.

_BTN2 (Right)_: Export data. Turns on both LEDs while executing `ESLO_EXPORT_DATA` and turns them off at the end.

_Time Found_: Enqueues `ESLO_TIME_FOUND`.

_Log Advertisement_: `ESLO_LogAdvertisement` is called when a bio-logger is recognized.

_Increment Time Event_: Adds `BASE_TIME_INTERVAL` (1000ms) to `curTime`.

##Set Time Details##
See old method: [Reading time from peripheral to update central](https://e2e.ti.com/support/wireless-connectivity/bluetooth-group/bluetooth/f/bluetooth-forum/1025080/cc2652r-reading-time-from-peripheral-to-update-central)

##Dumping Data##
`cd ~/Downloads`

 *  clear contents of screenlog.0
 *  connect device over USB

`ls /dev/tty.usbmodem*` (take the lower number)
 
 *  1: screen -L /dev/tty.usbmodemL1100NA51 115200
 *  2: screen -L /dev/tty.usbmodemL1100NM51 115200
 *  3: screen -L /dev/tty.usbmodemL1100MPN1 115200
 *  4: screen -L /dev/tty.usbmodemL1100LNK1 115200
 *  5: screen -L /dev/tty.usbmodemL1100LR91 115200
 *  6: screen -L /dev/tty.usbmodemL1100NM61 115200
 *  play program until end
 *  close iTerm with ctrl+a,k
