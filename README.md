# EFR32MG21_GenericFirmware

This is a generic build from reference!

![easyiot dongle](https://github.com/xsp1989/zigbeeFirmware/blob/master/Pic/easyiot%20Dongle.png)

EFR32MG210 target

Baudrate is 115200
|Standalone Bootloader| |
|---|---|
|NCP UART TX| PB1|
|NCP UART RX|PB0|

BUTTON_RESET is bootloader activiation pin/button
Version: x.xx.x
DCDC

Use "1. upload gbl" and "xmodem(128 byte)" to send bootloader ota file to device.

You can use SiLabs univeral flasher to update the file..
This is tested and working with HomeAssistant SILabs Multi-Protocol

# Install
Install the universal-silabs-flasher available on the Python wheel:
Command
|---|
|pip install universal-silabs-flasher|


Run firmware update
cd silabs-firmware

universal-silabs-flasher --device <serial-path> \
    flash --allow-cross-flashing --firmware <firmware-file>

Command
|---|
|universal-silabs-flasher --device /dev/ttyUSB0  flash --allow-cross-flashing --firmware xxxxxxxxxx.gbl|



