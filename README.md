# About

Board designed to interface with the [SparkFun DC/DC Converter Breakout] to provide external power (e.g. using LiPo batteries) for Raspberry Pis onboard the [Galactic Aztec] rocket.

The design does not incorporate the [ideal safety diode] as is advised for Raspberry Pi HATs, so be sure not to power the Raspberry Pi over USB at the same time powering using this board.

Custom EagleCAD parts on this board can be found in the [SDSU Rocket Eagle Libraries].


[SparkFun DC/DC Converter Breakout]: https://www.sparkfun.com/products/9370
[Galactic Aztec]: http://rocket.sdsu.edu/rockets
[SDSU Rocket Eagle Libraries]: https://github.com/twyatt/SDSURocket-Eagle-Libraries
[ideal safety diode]: https://github.com/raspberrypi/hats/blob/master/designguide.md#back-powering-the-pi-via-the-j8-gpio-header