# About

Board designed to provide external power (e.g. using 2-3S LiPo batteries) for Raspberry Pis onboard the [Galactic Aztec] rocket.

Supports 6-14 VDC input and allows tuning of output voltage between 4.64 and 5.27 VDC to the Raspberry Pi 5V GPIO pins.
**NOTE: RTRIM1 is incorrectly labelled as 2k and a 2.5k resistor should be used instead to put the output voltage at the expected range.**

The design features the [LTC4412HV] to act as an [ideal safety diode], which is advised for Raspberry Pi HATs.

Custom EagleCAD parts on this board can be found in the [SDSU Rocket Eagle Libraries].


[Galactic Aztec]: http://rocket.sdsu.edu/rockets
[LTC4412HV]: http://www.linear.com/product/LTC4412HV
[ideal safety diode]: https://github.com/raspberrypi/hats/blob/master/designguide.md#back-powering-the-pi-via-the-j8-gpio-header
[SDSU Rocket Eagle Libraries]: https://github.com/twyatt/SDSURocket-Eagle-Libraries