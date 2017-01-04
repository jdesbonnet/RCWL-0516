# RCWL-0516 information

Last update: 3 Jan 2017.

RCWL-0516 is a doppler radar microwave motion sensor module which can act as an alternative to a PIR motion sensor. 

![RCWL-0516 board](RCWL-0516-board.jpg)

At the heart of the module is a RCWL-9196. Unfortunately I can't find any datasheets or detailed information about this. The pin out is very similar to the BISS0001 PIR IC.

The unit I have was supplied by IC station (SKU 10630): http://www.icstation.com/rcwl-0516-microwave-motion-sensor-module-radar-sensor-body-induction-module-100ma-p-10630.html

Operating frequency: 5.8GHz ? I have been unable to verify this. I tried looking for a carrier wave with my HackRF One didn't find any obvious signal.

Working voltage: 4 - 28V. Provides a convenient 3.3V output to drive a MCU (good for 100mA ?).

## Board header

| Pin   | Function |
| ---   | --- |
| 3V3   | 3.3V regulated output. Max 100mA (?)                  |
| GND   | Ground                                                |
| OUT   | Trigger: high (3.3V) if motion detected. 0V normally. |
| VIN   | 4 - 28V supply voltage                                |
| CDS   |                                                       |

## Schematic

The only schematic I could find is very low resolution and it's hard to make out some of the text.

![RCWL-0516 schematic](RCWL-0516-schematic.jpg)

Q1 : looks like a mmbr951M high frequency NPN transistor. 

## RCWL-9196

This is the core IC of the board. The schematic says (in chinese) that it's similar to a BISS0001 PIR IC. But there are differences. Unfortunately I can't find any hard information (eg datasheet) on this. Nor can I find any information on the brand/company name "RCWL". 

| Pin number | BISS0001 | RCWL-9196 |
| --- | --- | --- |
| 1 | A Retriggerable & non-retriggerable mode select (A=1 : re-triggerable) | 3.3V regulated output (100mA max?) |
| 2 | VO Detector output pin (active high) | same |
| 3 | RR1 Output pulse width control (Tx)  | same |
| 4 | RC1 Output pulse width control (Tx)  |      |
| 5 | RC2 Trigger inhibit control (Ti)  |
| 6 | RR2 Trigger inhibit control (Ti) |
| 7 | Vss Ground | same |
| 8 | VRF RESET & voltage reference input (Normally high. Low=reset) |  Vin (4 - 28V) |
| 9 | VC Trigger disable input (VC > 0.2Vdd=enable; Vc < 0.2Vdd =disabled) |
| 10 | IB Op-amp input bias current setting  |
| 11 | Vdd Supply voltage | 3.3V regulated output (again?) |
| 12 | 2OUT 2nd stage Op-amp output|
| 13 | 2IN- 2nd stage Op-amp inverting input |
| 14 | 1IN+ 1st stage Op-amp non-inverting input |
| 15 | 1IN- 1st stage Op-amp inverting inpu |
| 16 | 1OUT 1st stage Op-amp output |



