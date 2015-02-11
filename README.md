# vscp_pic1_bootloader
VSCP Microchip PIC18F bootloader for use with VSCP over CAN 

This bootloader will work with the VSCP PIC1 algorithm of VSCP Works and is a For info see
 http://ww1.microchip.com/downloads/en/AppNotes/00247a.pdf 
this bootloader expects a slightly modified version of the bootloader 
described but in most aspects it is the same. 

Use file/export in MPLAB(x) after build to write the HEX file.
When programmed into a device and activated (byte 0 in EEPROM is 0xFF on startup) a confirm bootloader
mode CAN message with id= 0x000014nn and no data will be sent. Node id (nn) (least eight bits of id) is
taken from EEPROM byte 1.
If byte 0 in EEPROM is not oxFF on startup a normal boot of the relocated code will take place.
Hex files for device programming is available here
Hex files available here https://sourceforge.net/projects/m2m/files/VSCP%20Firmware/bootloader/


Ake Hedman
akhe@paradiseofthefrog.com
