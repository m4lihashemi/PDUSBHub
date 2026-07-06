# PDUSBHub

A custom 4-layer USB-C Power Delivery hub PCB based on the CH634W6G USB hub controller.  
The board includes USB-C PD power input, high-voltage power-path switching, onboard 5V buck regulation, USB SuperSpeed routing, and multiple downstream USB ports.

## Project Overview

This project is a USB-C hub design intended to combine high-speed USB data connectivity with a dedicated USB-C Power Delivery input. The board accepts a USB-C PD power source, routes the negotiated high-voltage rail through a controlled power path, and generates the internal 5V system rail using an onboard buck regulator.

The USB hub section is based on the CH634W6G controller and provides the upstream USB-C data interface along with multiple downstream USB ports.

## Main Features

- CH634W6G USB hub controller
- USB-C upstream data connection
- USB-C PD power input
- Up to 100W PD power path support
- High-voltage VHV rail routing
- Onboard 20V-to-5V buck regulator
- Multiple downstream USB ports
- 4-layer PCB design
- USB SuperSpeed differential pair routing
- Multi-layer GND pours and stitching
- Dedicated power routing for high-current paths
### Top View
<img src="images/Top_2D.png" width="700">
<img src="images/Top_3D.png" width="700">
### Bottom View
<img src="images/Bot_2D.png" width="700">
<img src="images/Bot_3D.png" width="700">


The design uses a dedicated USB-C PD input for the main power path. After PD negotiation, the high-voltage rail is routed through MOSFET-based power switching and then supplied to the buck converter. The buck converter generates the 5V system rail used by the USB hub controller and downstream power circuitry.

Basic power flow:

```text
USB-C PD Input
      ↓
Power Path MOSFETs
      ↓
VHV Rail
      ↓
Buck Converter
      ↓
5V System Rail
      ↓
USB Hub + Downstream Ports