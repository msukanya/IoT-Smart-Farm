/*****ESE516 A-Team Bootloader,CLI & OTAFU*****/

CLI Appcode  ::  WINC1500_HTTP_DOWNLOADER_EXAMPLE1
Bootloader      ::   SD_MMC_EXAMPLE_ESE516_SPRING2019

Addresses

Bootloader           :: 0x0000
Boot Status Flag   :: 0x9BC0
AppCode	            :: 0x9C00


There are two files in this package:

The one named "Firmware_AppCode&CLI" must be placed in the SD Card
along with the "Version.txt" file.

The one named "Firmware_LED_Blink" must be placed on the host server.

** Before placing the file in the SDCard & server respectively rename them 
to be "Firmware.bin"

Implementation

To see the implementation of the OTAFU, rename and place the 
"Firmware_AppCode&CLI" file in the SD CArd along with "Version.txt" 
file containing a version number higher than the one burnt on the board.

Rename and upload the "Firmware_LED_Blink" file in the Web Server.

Burn the Bootloader Code to the board. It will upload the bin file from the 
SD Card. Once the Firmware from the SD Card is uploaded, it will open the CLI;
type "menu" and press enter to get a list of the CLI commands.

From the Node Red Dashboard, press the OTAFU Button, teh Board will detect it,
it will then download the new file from the Web Server and go back to the 
Bootloader, which burns the new firmware to the board.
