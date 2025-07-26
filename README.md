# 6809 Monitor for Grant's board

This project is a small monitor for the SBC Grant's board 6809.
The ROM file prosduced is a 16kb size.

## i6809asm

This program is the 6809 assembler running on macOS used to assemble the source code of this maonitor and CocoBasic. It is derivated from the AS9 of the Grant's page. 
The i6809 assembler source code is available in my Github. Currently it is adapted to Xcode 16.2.

i6809asm is my own assmebler running on macOS.

## Grant's board memory map

- 0000-7FFF 32K RAM
- 8000-9FFF FREE SPACE (8K)
- A000-BFFF SERIAL INTERFACE (minimally decoded)
- C000-FFFF 16K ROM 

## SBC6809GMon

My own monitor, adapted here to this SBC 6809.

Make SBC6809GMon.bin :

- Open a BASH terminal 
- Enter to the folder SBC6809GMon
- Type: $ ./i6809asm SBC6809GMon.asm -bin
- This will produce a SBC6809GMon.bin file

SBC6809GMon.bin file produced is ready for your EEPROM burner with the correct size of 16384 bytes for a 16kB device.

## CocoBasic ROM

Make CocoBasic.bin :

- Open a BASH terminal 
- Enter to the folder CocoBasic
- Type: $ ./i6809asm CocoBasic.asm -bin
- This will produce a CocoBasic.bin file

CocoBasic.bin file produced is ready for your EEPROM burner with the correct size of 16384 bytes for a 16kB device.

## Terminal with screen command

Open a BASH terminal and type : 

$ screen /dev/my_usb_dev 115200

For example :

FTDI UART-USB: screen /dev/cu.usbserial-A5069RR4 115200


## Usefull links

Grant's 6-chip 6809 computer: Where I found CocoBasic and AS9. Very good page.

http://searle.x10host.com/6809/Simple6809.html


## Licence

This project is free and can be reused as you want without any restrictions.

2025 FAVARD Laurent 6809 projects.
