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


