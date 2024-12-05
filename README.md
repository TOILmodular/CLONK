# CLONK
This Eurorack module is based on the "Delayed Modulation" design from Music From Outerspace (Ray Wilson), combined with a simple squarewave sound source and an OTA filter.

<img height="500" src="https://github.com/user-attachments/assets/96db2e1a-1eb1-4bf5-bf9d-814900f98777">
<img height="500" src="https://github.com/user-attachments/assets/01fdf2ab-81c4-422e-82d2-e1cf02d714b9">

<img height="500" src="https://github.com/user-attachments/assets/e47612d5-983c-4505-95b2-b1791560fdae">
<img height="500" src="https://github.com/user-attachments/assets/58ad20f8-c897-42d6-bd8d-04398d937fd4">

The module can be used for metallic percussive sounds. It also has separate outputs from an attack-release/decay envelope generator, as well as from an LFO, modulated by that AD, which can be used itself as a CV modulation source.

The module also provides the option to add an external sound source, instead of the internal squarewave oscillator, and an external modulation source, instead of the internal LFO.

The following graph shows the signal flow within the module.
![Clonk - Signal Flow](https://github.com/user-attachments/assets/5e6d9713-41c8-45ad-9d51-30e10c813854)

A demo of the module is shown in the following YouTube video.

<img width="500" src="https://github.com/user-attachments/assets/ab825f1d-0798-4c44-b437-266522db0fba">

## Module Build and PCBs
I added two different versions for the control board in the folder GerberFiles, an "original", and a "Thonk" version.
Reason is that for my own module, I am using specific potentiometers - 16K4 series from Supertech Electronics - and 3.5mm jack sockets - MJ-355 from Marushin - available at my local electronics shop.

<img width="200" alt="CtrlPCB Orig" src="https://github.com/user-attachments/assets/b288da83-0ec3-4b87-95a7-00d5ec1ac544">

However, since most DIY projects for Eurorack modules out there are using potentiometers from ALPHA and so-called THONKICONN jacks, as they are provided by Thonk in the UK, I also created another control board PCB for the "Thonk" version with footprints for those components.

<img width="200" alt="CtrlPCB Thonk" src="https://github.com/user-attachments/assets/4a26d78b-67c7-48a9-96c5-5ca7b66637bc">

The main PCB is the same for both versions.

<img width="200" alt="MainPCB" src="https://github.com/user-attachments/assets/2b259b6d-f2c7-40ba-a6cd-c890b6a672f2">

I created the Gerber files with the online tool EasyEDA and ordered the PCBs at JLCPCB.

## Components
The module is mainly built out of THT components. The only exception are the 0.1 uF bypass caps for all the op amps, which are 1608 (0603) SMD components.

The original Pro Co guitar pedal circuit from 1978 used the LM308 op amp in the central distortion segment. Later redesigns contained the OP07 op amp instead, which I am also using in my module.
