- [Repository Info](#orgd6380e0)
- [Images](#orga66b571)
- [Schematic](#org639fc76)
- [PCB](#org10d0848)
- [Bill of Materials](#org05f62ac)
- [Development](#orgcf7187c)

    <!-- This file is generated automatically from metadata -->
    <!-- File edits may be overwritten! -->


<a id="orgd6380e0"></a>

# Repository Info

-   Project Name: honeycomb-pcb
-   Synopsis: PCB for each tessellated maze honeycomb.
-   Documentation Version: 1.0.0
-   Pcb Version: 1.0
-   Enclosure Version: 1.0
-   Supplemental BOM Version: 1.0
-   Release Date: 2024-07-16
-   Creation Date: 2024-06-28
-   Kicad Version: 7.0.11
-   License: BSD-3-Clause
-   URL: <https://github.com/janelia-kicad/honeycomb-pcb>
-   Author: Peter Polidoro
-   Email: peter@polidoro.io
-   Copyright: 2024 Howard Hughes Medical Institute
-   References:
    -   [W5500-EVB-Pico](https://docs.wiznet.io/Product/iEthernet/W5500/w5500-evb-pico)
    -   [TMC5130](https://www.analog.com/en/products/tmc5130.html)

![img](./documentation/pcb/raytrace.png)


<a id="orga66b571"></a>

# Images


<a id="org639fc76"></a>

# Schematic


<a id="org10d0848"></a>

# PCB


<a id="org05f62ac"></a>

# Bill of Materials


## Board

|    |
|--- |
|  |


## Supplemental

| Item | Synopsis                      | Manufacturer Part Number | Manufacturer   | Quantity | Cost  | Total |
|---- |----------------------------- |------------------------ |-------------- |-------- |----- |----- |
| 1    | FAN AXIAL 25X8MM 5VDC WIRE    | 255M                     | ebm-papst Inc. | 1        | 33.47 | 33.47 |
|      | Supplemental BOM Version: 1.0 |                          |                |          | Total | 40.11 |


<a id="orgcf7187c"></a>

# Development


## Install Guix

[Install Guix](https://guix.gnu.org/manual/en/html_node/Binary-Installation.html)


## Generate Output from KiCad


### Images

1.  3D Viewer

    Output directory: ../documentation/fabrication/gerbers
    
    -   pcb.png
    -   top.png
    -   bottom.png
    -   front.png
    -   back.png
    -   left.png
    -   right.png

2.  Trim

        make trimmed-images

3.  Schematic PDF

    File -> Plot
    
    Output directory: ../documentation/schematic
    
    -   Output format PDF
    -   Page Size = Schematic size
    -   Plot drawing sheet
    -   Output mode = Color
    -   Color theme = KiCad Default
    -   Default line width = 0.006 in

4.  Schematic SVG

    File -> Plot
    
    Output directory: ../documentation/schematic
    
    -   Output format SVG
    -   Page Size = Schematic size
    -   Plot drawing sheet
    -   Output mode = Color
    -   Color theme = Solarized Light
    -   Default line width = 0.012 in

5.  PCB SVG

    Add Edge.Cuts, holes, and dimensions to User.Drawings
    
    File -> Plot
    
    Output directory: ../documentation/pcb
    
    -   Plot format SVG
    -   Include Layers
        -   User.Drawings
        -   F.Silkscreen
        -   B.Silkscreen
        -   F.Fab
        -   B.Fab
    -   Plot on All Layers
        -   Edge.Cuts
    -   Plot footprint values
    -   Plot reference designators
    -   SVG Options
        -   Precision = 4
        -   Output mode = color
    
        make cropped-svg


### Gerber Files

File -> Fabrication Outputs -> Gerbers (.gbr)

Output directory: ../documentation/fabrication/gerbers

Include Layers:

-   F.Cu
-   F.Paste
-   F.Silks
-   F.Mask
-   B.Cu
-   B.Paste
-   B.Silks
-   B.Mask
-   Edge.Cuts - (contain the board outline/cutouts.)
-   In1.Cu, In2.Cu … - (needed for 4/6 layer designs.)

Options:

-   Select Plot reference designators, otherwise designators will not appear on silkscreen layers.
-   Select Check zone fills before plotting
-   Select Use Protel filename extensions, this is recommended as JLCPCB prefers Protel filename extensions.
-   Select Subtract soldermask from silkscreen, this ensures no silkscreen on pads.
-   Coordinate format 4.6 unit mm


### Drill and Map Files

Options:

-   Excellon drill file format
-   Check Use alternate drill mode for "Oval Holes Drill Mode".
-   Check Absolute for "Drill Origin".
-   Check Millimeters for "Drill Units".
-   Check Decimal format for "Zeros Format".
-   Gerber X2 map file format

Zip gerber files

    zip gerbers.zip gerbers/*


### BOM

Generate BOM from schematic editor using blank command line to create bom xml file.


### POS

File -> Fabrication Outputs -> Component Placement (.pos)

Output directory: ../documentation/fabrication/

Settings:

-   Format = CSV
-   Units = Millimeters
-   Files = Single file for board
-   Do not use drill/place file origin

Modify pos files:

-   Ref -> Designator
-   PosX -> Mid X
-   PosY -> Mid Y
-   Rot -> Rotation
-   Side -> Layer


## Edit metadata.org

    make metadata-edits


## Tangle metadata.org

    make metadata


## Edit project

    make kicad-edits
    exit
