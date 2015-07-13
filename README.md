# HC-06_Bluetooth
Android app to communicate comfortably with the HC-06.

# To change the name of your HC-06
Changing the name of your HC-06 device is a fairly simple process and can be done with whatever board you are using to manage your device in the first place. For this tutorial, we will be using an Arduino, however the same method is possible across any platform.

First off, plug in the board like you normally would (NOTE: do NOT use pins 0 or 1 on the Arduino for this step).

Next, we need to set up a SoftwareSerial connection with the device using the resources found in "SofwareSerial.h". If you require additional help to do this, a snippet of code can be found in the tutorial folder on this git page.

From here we can use the Arduino IDE's "Serial Monitor" to communicate with the board. Start by sending the board the string "AT" to enter command mode. Once you recieve a positive reply of "OK", you can proceed to change the name or any other attribute of the board.

Full list of AT commands:
AT : check the connection
AT+NAME<name>: Change name. No space between name and command.
AT+BAUD<x>: change baud rate, x is baud rate code, no space between command and code.
  1 set to 1200bps
  2 set to 2400bps 
  3 set to 4800bps 
  4 set to 9600bps (Default) 
  5 set to 19200bps 
  6 set to 38400bps 
  7 set to 57600bps 
  8 set to 115200bps
AT+PIN<xxxx>: change pin, xxxx is the pin, again, no space.
AT+VERSION
