# USB Host Library Rev.2.0

The code is released under the GNU General Public License.
__________
[![Build Status](https://travis-ci.org/felis/USB_Host_Shield_2.0.svg)](https://travis-ci.org/felis/USB_Host_Shield_2.0)

# Summary
This is Revision 2.0 of MAX3421E-based USB Host Shield Library for AVR's.

Project main web site is: <http://www.circuitsathome.com>.

Some information can also be found at: <http://blog.tkjelectronics.dk/>.

The shield can be purchased at the main site: <http://www.circuitsathome.com/products-page/arduino-shields> or from [TKJ Electronics](http://tkjelectronics.com/): <http://shop.tkjelectronics.dk/product_info.php?products_id=43>.

![USB Host Shield](http://shop.tkjelectronics.dk/images/USB_Host_Shield1.jpg)

For more information about the hardware see the [Hardware Manual](http://www.circuitsathome.com/usb-host-shield-hardware-manual).

# Developed By

* __Oleg Mazurov, Circuits@Home__ - <mazurov@circuitsathome.com>
* __Alexei Glushchenko, Circuits@Home__ - <alex-gl@mail.ru>
    * Developers of the USB Core, HID, FTDI, ADK, ACM, and PL2303 libraries
* __Kristian Lauszus, TKJ Electronics__ - <kristianl@tkjelectronics.com>
    * Developer of the [BTD](#bluetooth-libraries), [BTHID](#bthid-library), [SPP](#spp-library), [PS4](#ps4-library), [PS3](#ps3-library), [Wii](#wii-library), [Xbox](#xbox-library), and [PSBuzz](#ps-buzz-library) libraries
* __Andrew Kroll__ - <xxxajk@gmail.com>
    * Major contributor to mass storage code
* __guruthree__
    * [Xbox ONE](#xbox-one-library) controller support

### PS3 Library

These libraries consist of the [PS3BT](PS3BT.cpp) and [PS3USB](PS3USB.cpp). These libraries allows you to use a Dualshock 3, Navigation or a Motion controller with the USB Host Shield both via Bluetooth and USB.

In order to use your Playstation controller via Bluetooth you have to set the Bluetooth address of the dongle internally to your PS3 Controller. This can be achieved by first plugging in the Bluetooth dongle and wait a few seconds. Now plug in the controller via USB and wait until the LEDs start to flash. The library has now written the Bluetooth address of the dongle to the PS3 controller.

Finally simply plug in the Bluetooth dongle again and press PS on the PS3 controller. After a few seconds it should be connected to the dongle and ready to use.

__Note:__ You will have to plug in the Bluetooth dongle before connecting the controller, as the library needs to read the address of the dongle. Alternatively you could set it in code like so: [PS3BT.ino#L20](examples/Bluetooth/PS3BT/PS3BT.ino#L20).

For more information about the PS3 protocol see the official wiki: <https://github.com/felis/USB_Host_Shield_2.0/wiki/PS3-Information>.

Also take a look at the blog posts:

* <http://blog.tkjelectronics.dk/2012/01/ps3-controller-bt-library-for-arduino/>
* <http://www.circuitsathome.com/mcu/sony-ps3-controller-support-added-to-usb-host-library>
* <http://www.circuitsathome.com/mcu/arduino/interfacing-ps3-controllers-via-usb>

A special thanks go to the following people:

1. _Richard Ibbotson_ who made this excellent guide: <http://www.circuitsathome.com/mcu/ps3-and-wiimote-game-controllers-on-the-arduino-host-shield-part>
2. _Tomoyuki Tanaka_ for releasing his code for the Arduino USB Host shield connected to the wiimote: <http://www.circuitsathome.com/mcu/rc-car-controlled-by-wii-remote-on-arduino>

Also a big thanks all the people behind these sites about the Motion controller:

* <http://thp.io/2010/psmove/>
* <http://www.copenhagengamecollective.org/unimove/>
* <https://github.com/thp/psmoveapi>
* <http://code.google.com/p/moveonpc/>
