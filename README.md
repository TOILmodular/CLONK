# CLONK - A sound modulation and modification Eurorack module
This Eurorack module can be used as a sound source for metallic or bell-type percussive or more weird sounds. But it can also be used as a CV source for different modulations. It has separate outputs from an attack-release/decay envelope generator, as well as from a CV modulation source, shaped by the envelope generator combined with an LFO.

<img height="500" src="https://github.com/user-attachments/assets/96db2e1a-1eb1-4bf5-bf9d-814900f98777">
<img height="500" src="https://github.com/user-attachments/assets/01fdf2ab-81c4-422e-82d2-e1cf02d714b9">

<img height="500" src="https://github.com/user-attachments/assets/121af24c-5a0e-4e40-9d0a-23eb0d9c9b17">
<img height="500" src="https://github.com/user-attachments/assets/40bec67f-e790-4263-a8e9-e01e43feecfe">

The module is based on the "Delayed Modulation" design from Music From Outerspace (Ray Wilson), combined with a simple squarewave sound source and an OTA filter.

The module also provides the option to add an external sound source, instead of the internal squarewave oscillator, and an external modulation source, instead of the internal LFO.

## Features
- Simple internal sound source from a squarewave oscillator
- Optional input for any external sound source
- OTA filter with cutoff and resonance controls
- Internal LFO (selectable sine or square waveform, two selectable frequency ranges) for filter cutoff modutation
- Optional input for any external modulation source
- Simple AD/AR envelope generator, shaping the LFO modulation
- Trigger or gate selection for an incoming gate signal to switch between AD and AR
- Seprate outputs for the AD/AR and the enveloped LFO modulation
- Attenuator for the enveloped modulation signal

The following graph shows the signal flow within the module.
![Clonk - Signal Flow](https://github.com/user-attachments/assets/5e6d9713-41c8-45ad-9d51-30e10c813854)

The MOD OUT signal is a combination of the envelope generator and the LFO.
<img width="500" src="https://github.com/user-attachments/assets/0d7e4d1c-0b95-4035-998e-08b460999668">

A demo of the module is shown in the following YouTube video.

<img width="500" src="https://github.com/user-attachments/assets/af391b94-9147-4144-a77f-e59831f1d98e">

## Module Build and PCBs
NOTE: One part of the calibration of this module requires an oscilloscope.
This is for the internal LFO to oscillate evenly around 0V.
The quality of the oscilloscope is not important, a visualization of the waveform is sufficent.

I added two different versions for the control board in the folder GerberFiles, an "original", and a "Thonk" version.
Reason is that for my own module, I am using specific potentiometers - 16K4 series from Supertech Electronics - and 3.5mm jack sockets - MJ-355 from Marushin - available at my local electronics shop.

<img width="200" alt="CtrlPCB Orig" src="https://github.com/user-attachments/assets/56c3ae02-1453-4e9f-9317-ca60472b0b6e">

However, since most DIY projects for Eurorack modules out there are using potentiometers from ALPHA and so-called THONKICONN jacks, as they are provided by Thonk in the UK, I also created another control board PCB for the "Thonk" version with footprints for those components.

<img width="200" alt="FtrlPCB Thonk" src="https://github.com/user-attachments/assets/a3f29769-3bb6-48e2-8371-4461b016ce01">

The main PCB is the same for both versions.

<img width="200" alt="MainPCB" src="https://github.com/user-attachments/assets/bb5d955a-b880-4b6a-860a-3fa0a53ea9ce">

I created the Gerber files with the online tool EasyEDA and ordered the PCBs at JLCPCB.

## Components
The module contains several SMD components:
- LM13700 OTA IC (x2) - this IC is not being manufactured anymore as a THT component, but the SMD version is still available
- 0.1uF capacitor (x10) - used as bypass caps for all ICs
- MMBT3906 transistor (x3)

All other components in the module are through-hole.

## Calibration
There are two trimmers at the back of the module, labeled "MOD CV TRIM" and "SINE BIAS TRIM", which need to be adjusted after having completed the module.

#### SINE BIAS TRIM
This trimmer is used to have the sine wave from the LFO oscillate evenly around 0V.
1. Connect the module with a power supply in a way that the backside of the module is accessible.
2. Touch the two connection points marked in the image below with the two probe pins of an oscilloscope.
3. Check the waveform and adjust the bias via the trimmer to have the same maximum values for positive and negative voltage.
<img width="200" src="https://github.com/user-attachments/assets/d4d738e4-27c5-4537-8f6b-a268e56103f0">

#### MOD CV TRIM
This trimmer is used to adjust the output of the modulation CV to 0V when there is no gate signal applied.
1. Ensure that no cable is plugged into GATE IN.
2. Turn the knob MOD LEVEL fully clockwise.
3. Plug in a patch cable to MOD OUT.
4. Measure the voltage on that cable via a multimeter.
5. Adjust the trimmer to get 0V. 
