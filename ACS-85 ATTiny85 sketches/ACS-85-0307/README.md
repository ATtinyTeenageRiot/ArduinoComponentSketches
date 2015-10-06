# ACS-85-0307
or/and
==============


## Overview:
An or and an and
 
 a b c  out1 out2
 A    |  B   |  C   | Out1  |   Out 2
--- | --- | --- | --- | ---
 
## Pinout:
[![Pinout](https://github.com/robstave/ArduinoComponentSketches/blob/master/ACS-85%20ATTiny85%20sketches/ACS-85-0307images/acs-85-0307.png)] (https://github.com/robstave/ArduinoComponentSketches)


## Equivalent:
The equivalent circuit would look something like this
[![Pinout](https://github.com/robstave/ArduinoComponentSketches/blob/master/ACS-85%20ATTiny85%20sketches/ACS-85-0306/images/ACS-85-0307-orand.png)] (https://github.com/robstave/ArduinoComponentSketches)
 

## Examples:
 

## Strategy:
In this case, all the logic is in the loop. We are just reading the values and outputting them.  No interrupts or anything like that.
So this should be used as a non-time critical modulation.  There is no guarantee that signals will flip within a certain time limit.

## Improvements:
The highest frequencies that you can handle are going to depend on how fast the loop executes.  
 - Wrap the loop code into a while loop.   That would shave a few cycles off as loop would only be called once.  
 - Accumulate the bits and just mask off the last bit rather than all this ^ business.
 - Maybe save the value of port a and break if nothing changed?

