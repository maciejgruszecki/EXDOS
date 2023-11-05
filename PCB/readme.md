### Bill of materials (BOM)
| RefDes | Name | Value |
| ----- | ----- | ----- |
| C1, C2 | CAP100 | 470 nF |
| C3, C4, C5, C6, C7, C8 | CAP100 | 47 nF |
| C101 | CAP200RP | 470 µF / 25 V |
| C102, C103 | CAP100 | 100 nF |
| C104 | CAP200RP | 1000 µF / 10 V |
| D1, D2, D3, D4 | SR540 | 5 A Schottky diode |
| D101 | 1N5822 | 3 A Schottky diode |
| LED |  | red & green, common cathode |
| L1 | DE_1207 | 33 µH @ 3.2 A |
| Q1, Q2, Q3 | BC337 | or 2N2369 |
| R1, R5, R6, R7, R8 | RES100 | 1,5 kΩ |
| R2 | RES100 | 47 kΩ |
| R3, R9 | RES100 | 10 kΩ |
| R4 | RES100 | 1 kΩ |
| U101 | LM2596S-5.0 | |
| FDC | WD1772 | or VL1772 |
| GAL | GAL22V10 | or ATF22V10 |
| Memory | 27C256 | |
| 240A | 74LS240 | |
| 240B | 74LS240 | optional |
| 244 | 74LS244 | |
| 245 | 74LS245 | |
| 273 | 74LS273 | |
| PWR | HDR-1x2 | red jumper |
| EXP | HDR-1x2 | |
| DrvA, DrvB | HDR-1x3 | |
| MOT_A, SEL_A | HDR-1x3 | Cable mode |
| CFG | HDR-2x4 | Legacy drive config |
| J2 | HDR-2x8 | Memory config |
| J1 | 2x33 | Edge connector |
| J1A |2x32 | Expansion port |
| J1B | 1x2 | +5V for Expansion port |
| PWS | 4840-2201 | Power socket |
| SW1 | 1x2 | Power switch |
| J7 | HDR-2x17 | Floppy drives connector |
| J8 | | Floppy drives power |
| +12V | TESTPOINT | |
#### 240B jumpers
The chip 240B is optional. It is only needed in two situations:
* if you want to connect legacy Enterprise drive,
* there are connect more than 2 floppy drives.
#### Modes of floppy drives connection
* XT - Up to 4 drives can be connected (straight cable, drives setup by jumpers)
* AT - Up to 2 drives can be connected (twisted cable, both drives fixed as DS1)
#### A/B-B/A switch
* AB - standard order DS0=A, DS1=B
* BA - reverse order DS0=B, DS1=A
