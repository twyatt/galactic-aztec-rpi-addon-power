# About

[![OSHPark PCB Top Thumbnail](artwork/thumb_top.png?raw=true)](artwork/top.png?raw=true)
[![OSHPark PCB Bottom Thumbnail](artwork/thumb_bottom.png?raw=true)](artwork/bottom.png?raw=true)

Board designed to provide external power (e.g. using 2-3S LiPo batteries) for Raspberry Pis onboard the [Galactic Aztec] rocket.

Supports 6-14 VDC input and allows tuning of output voltage between 4.64 and 5.27 VDC to the Raspberry Pi 5V GPIO pins.
**NOTE: RTRIM1 is incorrectly labelled as 2k and a 2.5k resistor should be used instead to put the output voltage at the expected range.**

The design features the [LTC4412HV] to act as an [ideal safety diode], which is advised for Raspberry Pi HATs.

*The hope was to utilize the power switch-over features of the [LTC4412HV], allowing for the Raspberry Pi to be powered via USB and upon disconnecting, automatically switch over to the auxiliary power input, but in testing this feature did not function properly. Power was drawn from both sources when connected rather than completely switching between the available power sources.*

Custom EagleCAD parts on this board can be found in the [SDSU Rocket Eagle Libraries].


# Bill of Materials

| Qty | Name      | Description                                  | Part Number       | Vendor   |
|:---:|-----------|----------------------------------------------|------------------:|----------|
| 1   | CI2       | Capacitor 47µF 35V 63mA SMD                  | [493-2202-1-ND]   | DigiKey  |
| 1   | CI1       | Capacitor 22µF 35V 45mA SMD                  | [493-9805-1-ND]   | DigiKey  |
| 1   | R1        | Resistor 100kΩ 1/4W 1% 0603                  | [RHM100KADCT-ND]  | DigiKey  |
| 1   | IC1       | DC to DC Converter 6A                        | [555-1125-1-ND]   | DigiKey  |
| 1   | RTRIM1    | Resistor 2kΩ 0603                            | [P2.00KHCT-ND]    | DigiKey  |
| 1   | RTRIM2    | Resistor 2.49kΩ 0603                         | [RHM2.49KCFCT-ND] | DigiKey  |
| 1   | RTRIM3    | Potentiometer 1kΩ 10% 3/4W 20                | [987-1160-ND]     | DigiKey  |
| 1   | RTRIM_ALT | Resistor 1.33kΩ 0.1% 1/10W 0603              | [P1.33KDBCT-ND]   | DigiKey  |
| 1   | RTUNE     | Resistor 220Ω 1% 1/10W 0603                  | [RHM220CFCT-ND]   | DigiKey  |
| 1   | CTUNE     | Capacitor 3900pF 25V 5%                      | [445-2665-1-ND]   | DigiKey  |
| 2   | CO1, CO2  | Capacitor 47µF 35V 63mA SMD                  | [493-2202-1-ND]   | DigiKey  |
| 3   | C[2-4]    | Capacitor 10µF 16V 0603                      | [490-7198-1-ND]   | DigiKey  |
| 1   | R3        | Resistor 470kΩ 1% 1/4W 0603                  | [P470KBYCT-ND]    | DigiKey  |
| 1   | IC2       | LTC4412HV Source Selector Switch IC SOT-23-6 | [LTC4412HVIS6]    | DigiKey  |
| 1   |           | MOSFET P-Channel 1.8V Vdss=12V Id=6A SOT23-6 | [FDC606PCT-ND]    | DigiKey  |
| 1   |           | Capacitor 1000µF 20% 10V 310mA SMD           | [493-2171-1-ND]   | DigiKey  |
| 1   |           | Capacitor 820µF 20% 16V 80mΩ 510mA SMD       | [1189-2069-1-ND]  | DigiKey  |
| 1   |           | Capacitor 10uF 20% 16V 0603                  | [490-7198-1-ND]   | DigiKey  |
| 1   |           | Molex Mini Fit Jr. 4-pos Right Angle         | [WM1352-ND]       | DigiKey  |
| 1   | D4        | LED Red Vf=1.8V If=2mA 0603                  | [475-1195-2-ND]   | DigiKey  |
| 1   | R4        | Resistor 1.8kΩ 1/4W 1% 0603                  | [P1.8KBYCT-ND]    | DigiKey  |
| 1   |           | Header Stacking 2x20 Tall 23mm               | [1979]            | Adafruit |


[Galactic Aztec]: http://rocket.sdsu.edu/rockets
[LTC4412HV]: http://www.linear.com/product/LTC4412HV
[ideal safety diode]: https://github.com/raspberrypi/hats/blob/master/designguide.md#back-powering-the-pi-via-the-j8-gpio-header
[SDSU Rocket Eagle Libraries]: https://github.com/twyatt/SDSURocket-Eagle-Libraries
[493-2202-1-ND]: http://www.digikey.com/product-detail/en/UWT1V470MCL1GS/493-2202-1-ND/590177
[493-9805-1-ND]: http://www.digikey.com/product-detail/en/UWJ1V220MCL1GB/493-9805-1-ND/3963137
[RHM100KADCT-ND]: http://www.digikey.com/product-detail/en/ESR03EZPF1003/RHM100KADCT-ND/1983754
[555-1125-1-ND]: http://www.digikey.com/product-detail/en/APTS006A0X-SRZ/555-1125-1-ND/1766113
[P2.00KHCT-ND]: http://www.digikey.com/product-detail/en/ERJ-3EKF2001V/P2.00KHCT-ND/198219
[RHM2.49KCFCT-ND]: http://www.digikey.com/product-detail/en/MCR03ERTF2491/RHM2.49KCFCT-ND/2796475
[987-1160-ND]: http://www.digikey.com/product-detail/en/89PR1KLF/987-1160-ND/2408738
[P1.33KDBCT-ND]: http://www.digikey.com/product-detail/en/ERA-3AEB1331V/P1.33KDBCT-ND/3075785
[RHM220CFCT-ND]: http://www.digikey.com/product-detail/en/MCR03ERTF2200/RHM220CFCT-ND/2796470
[445-2665-1-ND]: http://www.digikey.com/product-detail/en/C1608C0G1E392J080AA/445-2665-1-ND/970490
[493-2202-1-ND]: http://www.digikey.com/product-detail/en/UWT1V470MCL1GS/493-2202-1-ND/590177
[490-7198-1-ND]: http://www.digikey.com/product-detail/en/GRM188C81C106MA73D/490-7198-1-ND/3900421
[P470KBYCT-ND]: http://www.digikey.com/product-detail/en/ERJ-PA3F4703V/P470KBYCT-ND/5036197
[LTC4412HVIS6]: http://www.digikey.com/product-detail/en/LTC4412HVIS6%23TRMPBF/LTC4412HVIS6%23TRMPBFCT-ND/3232334
[FDC606PCT-ND]: http://www.digikey.com/product-detail/en/FDC606P/FDC606PCT-ND/1626185
[493-2171-1-ND]: http://www.digikey.com/product-detail/en/UWT1A102MNL1GS/493-2171-1-ND/590146
[1189-2069-1-ND]: http://www.digikey.com/product-detail/en/16TKV820M10X10.5/1189-2069-1-ND/3986988
[490-7198-1-ND]: http://www.digikey.com/product-detail/en/GRM188C81C106MA73D/490-7198-1-ND/3900421
[WM1352-ND]: http://www.digikey.com/product-search/en?x=0&y=0&lang=en&site=us&keywords=538-39-30-1040
[475-1195-2-ND]: http://www.digikey.com/product-detail/en/LS%20L29K-H1J2-1-Z/475-1195-1-ND/810356
[P1.8KBYCT-ND]: http://www.digikey.com/product-detail/en/ERJ-PA3F1801V/P1.8KBYCT-ND/5036145
[1979]: http://www.adafruit.com/products/1979