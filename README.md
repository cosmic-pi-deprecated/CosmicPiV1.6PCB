# CosmicPiV1.6
Version 1.6 of the Cosmic Pi, learning the lessons from V2 and going back to something simpler. All the components are now on a single PCB with a snap-off for the SiPM elements. We have also moved to KiCad!

What do the signals do?
shapeout 1 & 2 - Shaped (i.e. amplified and stretched signal from the SiPMs - muon detection waveforms)
biasfb 1 & 2 - Feedback on the Vbias supply (i.e. to check that it's the right voltage)
inj led 1 & 2 - Light injector LEDs, allowing the operation of the SiPM to be checked (and calibrated) post-assembly
accint 1, 2 - Interrupts from the accelerometer, not really used for anything yet.
magint 3 - Interrupt from magnetometer
flag, boot0 - Signals to the Raspberry Pi, flag can be set by the STM32 to indicate a particular condition. Boot0 is used to set the boot mode of the STM32, for example when flashing.
vbusm otg dm otg dp - Vbus is the USB bus voltage detection line to the STM32 (i.e. in OTG mode, sense incoming voltage), DM and DP are the differential lines for USB communication.
swclk, swdio - These are the programming commands for the STM32, based on the ST-Link system. 
