- [Repository Info](#org53bed0e)
- [Images](#orgb9ab7fc)
- [Schematic](#orge2e3d74)
- [PCB](#org0a6b302)
- [Bill of Materials](#org299158d)
- [Development](#org038b3f9)

    <!-- This file is generated automatically from metadata -->
    <!-- File edits may be overwritten! -->


<a id="org53bed0e"></a>

# Repository Info

-   Project Name: honeycomb-pcb
-   Synopsis: PCB for each tessellated maze honeycomb.
-   Documentation Version: 1.0.0
-   Pcb Version: 1.0
-   Enclosure Version: 1.0
-   Supplemental BOM Version: 1.0
-   Release Date: 2024-07-12
-   Creation Date: 2024-06-28
-   Kicad Version: 7.0.11
-   License: BSD-3-Clause
-   URL: <https://github.com/janelia-kicad/honeycomb-pcb>
-   Author: Peter Polidoro
-   Email: peter@polidoro.io
-   Copyright: 2024 Howard Hughes Medical Institute
-   References:
    -   [TMC5130](https://www.analog.com/en/products/tmc5130.html)
    -   [W5500-EVB-Pico](https://docs.wiznet.io/Product/iEthernet/W5500/w5500-evb-pico)

![img](./documentation/pcb/raytrace.png)


<a id="orgb9ab7fc"></a>

# Images


<a id="orge2e3d74"></a>

# Schematic


<a id="org0a6b302"></a>

# PCB


<a id="org299158d"></a>

# Bill of Materials


## Board

|    |
|--- |
|  |


## Supplemental

| Item | Synopsis                              | Manufacturer Part Number | Manufacturer        | Quantity | Cost  | Total |
|---- |------------------------------------- |------------------------ |------------------- |-------- |----- |----- |
| 1    | FAN AXIAL 25X8MM 5VDC WIRE            | 255M                     | ebm-papst Inc.      | 1        | 33.47 | 33.47 |
| 2    | CONN RCPT HSG 2POS 1.25MM             | 5055650201               | Molex               | 1        | 0.32  | 0.32  |
| 3    | CONN SOCKET 26-30AWG CRIMP GOLD       | 5054311100               | Molex               | 2        | 0.30  | 0.60  |
| 4    | Hex Standoff Threaded M2 Brass 8.00mm | 970080244                | Würth Elektronik    | 3        | 0.65  | 1.95  |
| 5    | MACH SCREW PAN HEAD PHILLIPS M2 12mm  | MPMS 002 0012 PH         | B&F Fastener Supply | 3        | 0.32  | 0.96  |
| 6    | MACH SCREW PAN HEAD PHILLIPS M2 5mm   | MPMS 002 0005 PH         | B&F Fastener Supply | 3        | 0.17  | 0.51  |
| 6    | CONN RCPT HSG 2POS 1.50MM             | 0874390200               | Molex               | 1        | 0.22  | 0.22  |
| 7    | PICO-SPOX 874210000, 24 AWG,UL10      | 0797580016               | Molex               | 2        | 1.04  | 2.08  |
|      | Supplemental BOM Version: 1.0         |                          |                     |          | Total | 40.11 |


<a id="org038b3f9"></a>

# Development


## Install Guix

[Install Guix](https://guix.gnu.org/manual/en/html_node/Binary-Installation.html)


## Edit metadata.org

    make metadata-edits


## Tangle metadata.org

    make metadata


## Edit project

    make kicad-edits
    exit
