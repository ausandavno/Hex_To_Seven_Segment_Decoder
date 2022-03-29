# HEX_TO_7SEG_DECODER_COMMON_ANODE_V2.0

A WinCUPL project enabling an ATF16V8B chip to emulate a 74LS47 seven segment display decoder IC with additional/new hex-output functionality. 

Version 2.0 implements the Blanking Input functionality of the 74LS47.

See [my website](https://www.andavno.com/?p=672) for a description of v2.0 changes.

## Software

Project files created under WinCUPL version 5.30.4

WinCUPL can be found on the [PLD Design Resources page](https://pages.github.com/) of the Microchip website as of 2020/10/8.

[Direct link to WinCUPL installer](http://ww1.microchip.com/downloads/archive/awincupl.exe) that may or may not break in future. Microchip suggests serial number 60008009.

## Hardware Emulation

The ATF16V8B PLD is programmed to emulate the pin-out of the 74LS47 seven segment display decoder IC. This can only be a close approximation as the ATF16V8B is a 20 pin device and the 74LS47 is a 16 pin device. 

See comparison:
![Rev0 Image 1](../COMMON_ANODE_v2.0/Images/74LS47_to_ATF16V8B_Pin_Assignment_v2.0.png)

Wire the ATF16V8B chip according to the pinout above.

## Software Emulation

The ATF16V8B is programmed to mimic the 74LS47 seven segment display decoder IC with expanded functionality in the form of an ability to display hexadecimal characters corresponding to BCD inputs in the hexadecimal range.

This v2.0 code implements Blanking Input functionality. 

The 74LS47 Ripple Blanking Input, Lamp Test Input, and Ripple Blanking Output are NOT implemented to keep code size down.

The ATF16V8B is programmed to produce inverted outputs suitable for driving a Common Anode seven segment display (i.e. to mimic the 74LS47).

## Implementation

The "HEX_TO_7SEG_DECODER_COMMON_ANODE_V2.0.jed" file is the compiled output of the WinCUPL project.

The "HEX_TO_7SEG_DECODER_COMMON_ANODE_V2.0.jed" file can be directly used to program an ATF16V8B PLD chip and achieve conversion of hexadecimal-range BCD inputs for display of hexadecimal characters on a Common Anode seven segment display. 

Normal Function:
![Rev0 Image 1](../COMMON_ANODE_v2.0/Images/IMG_6497s.jpg)

With Blanking Input:
![Rev0 Image 1](../COMMON_ANODE_v2.0/Images/IMG_6498s.jpg)

See [my website](https://www.andavno.com/?p=672) for a guide on how to use WinCUPL to compile the project files and how to program the ATF16V8B.
