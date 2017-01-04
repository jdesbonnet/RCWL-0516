# RCWL-0516 information

Last update: 3 Jan 2017.

RCWL-0516 is a doppler radar microwave motion sensor module which can act as an alternative to a PIR motion sensor. 

At the heart of the module is a RCWL-9196. Unfortunately I can't find any datasheets or detailed information about this. The pin out is very similar to the BISS0001 PIR IC.

The unit I have was supplied by IC station (SKU 10630): http://www.icstation.com/rcwl-0516-microwave-motion-sensor-module-radar-sensor-body-induction-module-100ma-p-10630.html

Operating frequency: 5.8GHz ? I have been unable to verify this. I tried looking for a carrier wave with my HackRF One didn't find any obvious signal.

Working voltage: 4 - 28V. Provides a convenient 3.3V output to drive a MCU (good for 100mA ?).
