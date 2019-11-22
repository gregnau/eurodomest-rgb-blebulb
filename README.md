# Eurodomest RGB LED Bluetooth BLE bulb linux tool

![alt text](https://raw.github.com/gregnau/eurodomest-rgb-blebulb/master/eurodomest-rgb-blebulb.png "Eurodomest RGB Led BLE lamp")

It is basically a wrapper around the 'gatttool' from the BlueZ package on Linux.
Provides easy control for the Eurodomest RGB Bluetooth LE bulbs from command line.
Fast enough for continous dimming of the lamp, therefore it can be used for
simple effects also. Running nice on desktops/laptops and Raspberry Pi/Orange Pi.

```Usage: blebulb [OPTION]... [VALUE]...
Control Eurodomest BLE RGB lamp.

Options:
  -s, --set #w	    		Set white level from 0-256
	    #r #g #b    	Set an RGB level value (white off)
	    #r #g #b #w 	Set and RGB-W level

  -f, --fade #w	    		Fade white level from 0-256
	    #r #g #b    	Fade to an RGB level value (white stays off)
	    #r #g #b #w 	Fade to an RGB-W level (RGB + White)

  -c, --color $name		Set colors by name; like 'maroon', 'olive', 'aqua' ...
  -h, --help	        	Display this help text

Examples:
  blebulb --set 100		Setting the white leds to 100
  blebulb -s 25 25 25		Mix a custom color with RGB code
  blebulb -s 225 255 225 80	Custom ambient color with RGB-W code
  blebulb -f 128 225 128 30	Fade to a custom color from current state
  blebulb --fade 255		Fade to a custom color from current state```
