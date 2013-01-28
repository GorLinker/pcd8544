PDC8544 LCD python bindings for the Raspberry Pi
================================================

Documentation and Python library module for interfacing a PCD8544 LCD 
screen to a Rasbperry Pi.

![PCD8544](https://raw.github.com/rm-hull/pcd8544/master/doc/pcd8544.png) ![Spec](https://raw.github.com/rm-hull/pcd8544/master/doc/tech-spec/spec.png)

Further technical details for the LCD screen can be found in the 
[datasheet](https://raw.github.com/rm-hull/pcd8544/master/doc/tech-spec/datasheet.pdf) [PDF].

Pre-requisites
--------------
Compile and install the wiringPi python bindings from https://github.com/rm-hull/wiringPi

Building and installing the software
------------------------------------
After having cloned from github:

     $ python setup.py clean build
     $ sudo python setup.py install

This should install the files in your local dist-files ares (somewhere
like `/usr/local/lib/python2.7/distfiles/pcd8544`).

Next, test at the hardware and software is working:

    $ cd examples
    $ sudo ./alphabet-text.py

Most of the ASCII character set should be displayed. There are a few
other examples of graphics rendering in the same directory.

Wiring schematic
----------------
There appears to be different pin-out configurations on PCD8544 modules - beware!

![Wiring Schematic](https://raw.github.com/rm-hull/pcd8544/master/doc/wiring-diagram.png)

Modified for my wiring setup from an SVG from http://shiro.be/ - all 
rights of the original author respected.

Stripboard Layout
-----------------
With 4 push-buttons, resistor values 10K.

![Stripboard Layout](https://raw.github.com/rm-hull/pcd8544/master/doc/schematic_bb.png)

The finished article:

![Built stripboard](https://github.com/rm-hull/pcd8544/blob/master/doc/images/IMG_2544.JPG)

TODO
----
* Documentation

* More examples

* Implement video ram & get/set_pixel

References
----------
* http://binerry.de/post/25787954149/pcd8544-library-for-raspberry-pi

* http://www.avdweb.nl/arduino/hardware-interfacing/nokia-5110-lcd.html

* http://www.raspberrypi.org/phpBB3/viewtopic.php?f=32&t=9814&start=100

* https://projects.drogon.net/raspberry-pi/wiringpi/pins/

* http://www.henningkarlsen.com/electronics/t_imageconverter_mono.php

* http://fritzing.org
