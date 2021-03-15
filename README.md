# This Repo is for ESP8266 MicroPython Scripts and Knowledge

## How to wire ESP8266 to program with Micropython
- Vcc   -> Vcc
- Gnd   -> Gnd
- REST  -> Vcc
- CH_P0 -> Vcc
- GPIO0 -> Gnd for Flashing 
- Tx    -> Rx of USB cable
- Rx    -> Tx of USB cable

### Flashing
- Make sure GPIO0 is grounded and power cycled for good measure.
- Loading firmware instructions: [Here](https://docs.micropython.org/en/latest/esp8266/tutorial/intro.html)
- Firmware Download: [Here](https://micropython.org/download/esp8266/)

_Example command_
```
pip install esptool
esptool.py --port /dev/ttyUSB0 erase_flash
esptool.py --port /dev/ttyUSB0 --baud 460800 write_flash --flash_size=detect 0 esp8266-20170108-v1.8.7.bin
```


## MicroPython gotchas with Pycharm plugin
- You might need to manually enter the path for the ESP8622 for example `/dev/ttyUSB0
- You might also need to add the current user to the dialout group if you get permission errors.  Don't forget to restart after.
- To upload make sure GPIO0 is not at Gnd
