How to update the firmware of OLIMEXINO-NANO-GSM (the board has SIM800H)?

You would need to download a tool used to upload to the module and also appropriate firmware version. These are hosted as zip archives here at GitHub.

You would need to establish a serial connection. In this example we use a cable called USB-Serial-Cable-F. We also need OLIMEXINO-NANO-BAT module and a charged battery.

Connect the wires of the Serial cable to the UART connector (the pins on the side of the SIM card connector) as follows:

Note!!! On UART connector Pin 1 is on the side of GPIO CON3, and Pin 4 - on the side of GPIO CON4.

Red wire (TX) to Pin 2
Green wire (RX) to Pin 3
Blue wire (GND) to Pin 4

To power the setup we use a battery plugged in the OLIMEXINO-NANO-BAT module connected to the extensions of the OLIMEXINO-NANO-GSM. The BAT_SWITCH must be in position ON. In case we need a reset we can toggle BAT_SWITCH OFF and ON again.

Start the "..\SIMCom_SIM800H_EAT_flash_Tool_V1.01\SIMCom_SIM800H_EAT_flash_Tool.exe" tool. Configure the program:
1) Options --> ...
  1.1) If the "USB Download/Readback" option is checked --> uncheck it.
  1.2) Baudrate --> Set the baudrate. Recommended for this module is 57600.
  1.3) COM Port --> Select the one of the USB-Serial-Cable.
2) Select the configuration file of the firmware you want to download. Scatter/Config File... (..\1308B06SIM800H32\1308B06SIM800H32.cfg)
3) Trigger the updating by click on Download button.
4) Power-up the board by holding the power button on the Olimexino-NANO-GSM module.
5) Wait until the process is finished. Since the baudrate is low it is a slow process taking up to 15 minutes.

2014/10/6
Stanimir Petev, Olimex
