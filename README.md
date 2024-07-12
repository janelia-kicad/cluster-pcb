- [Repository Info](#org5320e88)
- [Images](#orgb6f5aa0)
- [Schematic](#org25409cb)
- [PCB](#org7ecc2d9)
- [Bill of Materials](#org95cf775)
- [Development](#org5caec1f)

    <!-- This file is generated automatically from metadata -->
    <!-- File edits may be overwritten! -->


<a id="org5320e88"></a>

# Repository Info

-   Project Name: honeycomb-pcb
-   Synopsis: Connects a microcontroller and power to multiple tmc5130-uart boards.
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
    -   [RP2040](https://www.raspberrypi.com/documentation/microcontrollers/rp2040.html)

![img](./documentation/pcb/raytrace.png)


<a id="orgb6f5aa0"></a>

# Images


<a id="org25409cb"></a>

# Schematic


<a id="org7ecc2d9"></a>

# PCB


<a id="org95cf775"></a>

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


<a id="org5caec1f"></a>

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
