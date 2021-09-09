# Pocket-FT8
A pocket sized FT8 Transceiver utilizing Teensy 3.6, Si4735 and Si5351 technology.

Pocket FT8: A Palm Size FT 8 Transceiver

Copyright (C) 2021, Charles Hill

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

Please use this software at your own risk

Project Features:

FT8 Message Transmit and Receive

Small Size, 3.5” X 2.75” X 1.125”

100 mW power output @ 50 ohm load

1 uVolt Receiver Sensitivity

Single 5 volt power input, battery or wall wart

Silicon Labs Technology, Si4735 SSB Receiver & Si5351 Transmit FSK Clock

SD Card Contact Logging

320 X 480 Resistive  Color Touch Screen


Attributions:

This project is based on two significant software projects:

 Si4735 Library developed by Ricardo Caritti: https://github.com/pu2clr/SI4735

 FT8 Decoding Library by Karlis Goba: https://github.com/kgoba/ft8_lib

DSP Audio Architecture
Decoding FT8 requires significant data storage and processing speed.

In order to optimize both program storage and processing speed requirements so that the Teensy 3.6 is not over taxed, the Teensy Audio Library has been modified to allow Analog to Digital conversion to be run at the rate of 6400 samples per second. This allows audio data processing to be done at 3200 Hz. The 3200 Hz audio processing with a 2048 FTT to process the received audio for FT8 decoding yields a bin spacing of 3.125 Hz.

The algorithms developed by Karlis Goba use the 3.125 Hz spaced FFT bins to be screened in both frequency and time so that errors in symbol frequency and time reception  can be overcome to provide really great FT8 decoding. The end spacing of the FT8 algorithms is 6.25 Hz.

The Teensy 3.6 source code and all other project documentation is packaged in the "Pocket_FT8_Publish.zip" archive.
