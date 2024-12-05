when you order this board at JLCPCB, make sure to add a note to tell them that they don't have to bake the LEDs before assembly so you can use economic PCBA.


there are 3 solder jumpers on the back. one for each row of indicator LEDs and one for selecting which power input should drive the motors.

to drive the motors with 5V from USB or from the connected 5V JST plug input, close the side labeled 5V/USB.
to drive the motors with an external voltage supply up to 30V (maximum rated voltage of the AO3400 MOSFETS), close the side labeled VIN.
VIN will now only drive the transistor inputs, you will have to provide a separate 5V supply for the microcontroller.
If both sides are closed, the VIN JST plug can be used as a vertical 5V power input to drive the motors and the ESP32/shift registers with the same 5V supply.


this board uses the onboard USB functionality of the ESP32-S3 for programming and debugging. 
if you run into issues with flashing new firmware while the board is outputting on the USB serial port, press the boot button while you begin flashing the firmware.
