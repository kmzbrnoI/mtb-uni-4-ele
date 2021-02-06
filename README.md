MTB-UNI v4 PCB
==============

MTB-UNI is an universal IO module featuring 16 digital inputs and 16 digital
outputs. It communicates over [MTBbus](https://mtb.kmz-brno.cz/bus) (RS485).
The module is designed for controlling of the model railroad accessories (such
as turnouts or occupancy detectors), however is could be used generally in
any other application.

This repository contains schematics & PCB layout of MTB-UNI v4 PCB. Firmware
for main MCU ATmega128 is available
[here](https://github.com/kmzbrnoI/mtb-uni-4-fw). More information about
MTB in available [here](https://mtb.kmz-brno.cz/).

## Design

Schematics & PCB are designed in Eagle 9.

## Production

PCB is prepared to be automatically assembled in [JLCPCB](https://jlcpcb.com/).
SMD parts on bottom side should be assembled. Each SMD part has its `LCSC_ITEM`
attribute set.

## Parameters

 * Input voltage: 7–17 V.
   Protection: when > 18 V is applied, input is shorted. Afterwards, current
   is limited by PTC fuse on input to 200 mA. Changed-polarity protection.
 * Max current consumption: 120 mA.
 * Outputs: 16 open collectors. Max current: 200 mA / pin. 500 mA per 8 pins.
   Active-low. Pull-up should be in receiving device.
 * Inputs: 16 active-low digital inputs. Pulled up to +5 V internally.
   Max 5.1 V on input. When bigger voltage applied, input is shorted, current
   is limited to 50 mA by PTC fuse.
 * ULN modules & RS485 drivers are in DIL packages & sockets, so they could
   be easily replaced in case of failure.
 * Screw sockets or connectors could be variably assembled on inputs & outputs
   based on user requirements.

## Authors

MTB-UNI v4 module is designed by:

 * [Laboratory of railroad control](https://lrkv.pef.mendelu.cz/) Mendel University Brno,
 * [Model Railway Club Brno](https://www.kmz-brno.cz/).

People:

 * Jan Horáček
 * Robert Čížek

## License

Content of the repository is provided under [Creative Commons
Attribution-ShareAlike 4.0
License](https://creativecommons.org/licenses/by-sa/4.0/) as openhardware
project. You may download any data, contribute to the project, create PCB
yourself or even sell it yourself.
