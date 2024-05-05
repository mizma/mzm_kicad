# mzm_kicad

KiCad library for various projects.  mainly keyboard and arcade controller related.

## Licenses

The original data marked as created by myself falls under CC-BY-SA/MIT dual license.

All other content aggregated into this repository follows the original License set
by their respective authors/project owner.  See the LICENSE files in their respective
directories for their licenses.

## Library Listing and sources

Check for the Licenses for each item.

### RP2040.pretty

Symbol library and basic component footprint obtained from 
[Hardware Design with RP2040](https://datasheets.raspberrypi.com/rp2040/hardware-design-with-rp2040.pdf)
[minimal design example schematics and layout files](https://datasheets.raspberrypi.com/rp2040/Minimal-KiCAD.zip)

### External Repositories

* ai03-2725_Type-C.pretty
    * [ai03-2725/Type-C.pretty](https://github.com/ai03-2725/Type-C.pretty)
* daprice_keyswitches.pretty
    * [daprice/keyswitches.pretty](https://github.com/daprice/keyswitches.pretty)
* kiswitch_kiswitch
    * [kiswitch/kiswitch](https://github.com/kiswitch/kiswitch)

### mzm_LCSC

Imported from [LCSC](https://www.lcsc.com/).  Useful for JLCPCB PCB Assembly service since 
JLCPCB uses LCSC and their footprint library as their Pick-and-Place machine coordinates.

See the LCSC Part information section below for the LCSC Part number information for the
list of parts used in this library.

### mzm_misc

Random footprint libraries created by @mizma.

## LCSC Part information

Some Footprint parts I use on Keyboard/GP2040-CE projects

| Part Number   | Footprint | Description |
| :--           | :--       | :--         |
| C1525         | `Capacitor_SMD:C_0402_1005Metric` | 100n Caps SMD |
| C1570         | `Capacitor_SMD:C_0402_1005Metric` | 30p Caps SMD |
| C52923        | `Capacitor_SMD:C_0402_1005Metric` | 1u Caps SMD |
| C11702        | `Resistor_SMD:R_0402_1005Metric` | 1k Resistor SMD |
| C23162        | `Resistor_SMD:R_0603_1608Metric` | 4.7k Resistor SMD |
| C25744        | `Resistor_SMD:R_0402_1005Metric` | 10k Resistor SMD |
| C25905        | `Resistor_SMD:R_0402_1005Metric` | 5.1k Resistor SMD |
| C138021       | `Resistor_SMD:R_0402_1005Metric` | 27ohm Resistor SMD |
| C2040         | `RP2040:RP2040-QFN-56` | RP2040 MCU |
| C134139       | `Package_TO_SOT_SMD:SOT-23-5` | 300mA Capacitor-Free Low Dropout Voltage Regulator, Fixed Output 3.3V, SOT-23-5 |
| C9002         | `Crystal:Crystal_SMD_3225-4Pin_3.2x2.5mm` | Four pin crystal, GND on pins 2 and 4 |
| C97521        | `Package_SO:SOIC-8_5.23x5.23mm_P1.27mm` | 128Mb Serial Flash Memory, Standard/Dual/Quad SPI, SOIC-8 |
| C165948       | `HRO-TYPE-C-31-M-12` | USB-C Connector SMD |
| C2848619      | `HRO_USB-C-SMD_TYPE-C-31-M-13C` | USB-C Connector SMD-board sink |
| C605398       | `SOT-723_L1.2-W0.8-P0.40-LS1.2-BR` | ESD7L5.0DT5G 10.4V 5.4V 5V SOT-723-3 Electrostatic and Surge Protection (TVS/ESD) ROHS |

### Adding parts in JLCPCB PCBA service

Put the parts in BOM csv files with the Comment, Designaor, Footprint and LCSC part number 
as shown in example below.

~~~csv
Comment,Designator,Footprint,LCSC
1u,"C1,C9,C15,C16",Capacitor_SMD:C_0402_1005Metric,C52923
30p,"C13,C14",Capacitor_SMD:C_0402_1005Metric,C1570
100n,"C2,C3,C4,C5,C6,C7,C8,C10,C11,C12",Capacitor_SMD:C_0402_1005Metric,C1525
27,"R1,R2",Resistor_SMD:R_0402_1005Metric,C138021
10k,R3,Resistor_SMD:R_0402_1005Metric,C25744
1k,"R4,R7",Resistor_SMD:R_0402_1005Metric,C11702
5.1k,"R5,R6",Resistor_SMD:R_0402_1005Metric,C25905
4.7k,"R8,R9",Resistor_SMD:R_0603_1608Metric,C23162
RP2040,U1,RP2040:RP2040-QFN-56,C2040
TLV73333PDBV,U2,Package_TO_SOT_SMD:SOT-23-5,C134139
W25Q128JVS,U3,Package_SO:SOIC-8_5.23x5.23mm_P1.27mm,C97521
HRO-TYPE-C-31-M-12,USB1,Type-C:HRO-TYPE-C-31-M-12-Assembly,C165948
Crystal_GND24,Y1,Crystal:Crystal_SMD_3225-4Pin_3.2x2.5mm,C9002
~~~

The CPL file should look something like the following.

~~~csv
Designation,Val,Package,Mid X,Mid Y,Rotation,Layer
C1,1u,C_0402_1005Metric,141.436,-66.986,90,top
C2,100n,C_0402_1005Metric,137.372,-66.069,90,top
C3,100n,C_0402_1005Metric,132.292,-69.498,180,top
C4,100n,C_0402_1005Metric,142.805,-73.794934,0,top
C5,100n,C_0402_1005Metric,132.447,-73.795732,180,top
C6,100n,C_0402_1005Metric,138.134,-79.021,-90,top
C7,100n,C_0402_1005Metric,142.833,-69.879,0,top
C8,100n,C_0402_1005Metric,142.833,-68.863,0,top
C9,1u,C_0402_1005Metric,140.42,-66.097,90,top
C10,100n,C_0402_1005Metric,139.15,-79.021,-90,top
C11,100n,C_0402_1005Metric,136.356,-65.49,90,top
C12,100n,C_0402_1005Metric,133.308,-59.465,0,top
C13,30p,C_0402_1005Metric,135.672,-80.545,0,top
C14,30p,C_0402_1005Metric,138.769,-83.339,-90,top
C15,1u,C_0402_1005Metric,147.306,-63.529,180,top
C16,1u,C_0402_1005Metric,147.306,-68.863,180,top
R1,27,R_0402_1005Metric,138.388,-65.94,-90,top
R2,27,R_0402_1005Metric,139.404,-65.94,-90,top
R3,10k,R_0402_1005Metric,123.527,-61.116,0,top
R4,1k,R_0402_1005Metric,137.118,-80.037,90,top
R5,5.1k,R_0402_1005Metric,139.408,-59.338,180,top
R6,5.1k,R_0402_1005Metric,143.726,-60.1,-90,top
R7,1k,R_0402_1005Metric,120.862,-61.116,180,top
R8,4.7k,R_0603_1608Metric,126.708,-75.4,0,top
R9,4.7k,R_0603_1608Metric,126.708,-73.876,180,top
U1,RP2040,RP2040-QFN-56,137.621,-72.795,0,top
U2,TLV73333PDBV,SOT-23-5,146.836,-66.2015,90,top
U3,W25Q128JVS,SOIC-8_5.23x5.23mm_P1.27mm,129.708,-63.021,-90,top
USB1,HRO-TYPE-C-31-M-12,HRO-TYPE-C-31-M-12-Assembly,142.204,-55.034,180,top
Y1,Crystal_GND24,Crystal_SMD_3225-4Pin_3.2x2.5mm,136.522,-83.255,-90,top
~~~

Columns should be adjusted from the original KiCAD export file since
JLCPCB requires some columns.  See JLCPCB website for more details.
