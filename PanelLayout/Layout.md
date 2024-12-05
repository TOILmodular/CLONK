## Panel Layout for PCB

The panel dimensions provided in the section "Original Design" below are based on my own module build, since I am not following the standard HP (1HP eq. 5.08mm) size. An alternative by building an HP-standard size panel can be found in the section "HP Standard Design" further below.

### Original Design
Coordinates given in the table fit to the layout of components given in the PCBc in folder GerberFiles.
The layout is slightly different for both versions due to different positions of the output LEDs. Details are given in the coordinates table below.

Panel size: 55mm x 128.5mm

The numbers in the table are refering to the numbers in the picture below.
Coordinates origin is the lower left corner of the panel.


| No. | X-coord. [mm] | Y-coord. [mm] | Comment |
| --- | --- | --- | --- |
| 1 | 27.5 | 110 | MOD FREQ Pot |
| 2 | 10 | 103 | ATTACK Pot |
| 3 | 45 | 103 | OSC FREQ Pot |
| 4 | 27.5 | 85 | CUTOFF Pot |
| 5 | 10 | 78| DECAY Pot |
| 6 | 45 | 78 | RES Pot |
| 7 | 10 | 56 | FAST/SLOW Switch |
| 8 | 27.5 | 56 | SIN/SQR Switch |
| 9 | 45 | 56 | GATE/TRIG Switch |
| 10 | 10| 43 | LED |
| 11 | 45 | 43 | GATE IN Jack |
| 12 | 27.5 | 36 | MOD LEVEL Pot |
| 13 | 10 | 29 | EXT MOD Jack |
| 14 | 45 | 29 | EXT IN Jack |
| 15 | 10 | 15 | AD OUT Jack |
| 16 | 27.5 | 15 | MOD OUT Jack |
| 17 | 45 | 15 | OUT Jack |

<img height="1200" src="https://github.com/user-attachments/assets/34dc437e-12b8-4f9b-b025-d02a5e402545">

### HP Stadard Design
For building the panel with a size following the HP standard, you can use the panel Gerber files provided in the folder "GerberFiles".

There are two versions ("Orig" and "Thonk"), since the positions of some of the LEDs are slightly different, due to the jack size difference for the two versions.

I ordered my own panel via such gerber file built out of PCB material.

| Parameter | Value |
| --- | --- |
| Width | 12HP |
| Pot hole diameter | 8mm |
| Jack hole diameter | 6.1mm |
| Switch hole diameter | 6.5mm |
| LED hole diameter  | 3.1mm|
| Mounting hole diameter | 3.2mm|
