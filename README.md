<div>
  <picture>
    <source media="(prefers-color-scheme: light)" srcset="docs/logo_terein_light.svg">
    <img alt="tiny corp logo" src="docs/logo_terein_dark.svg" width="300px">
  </picture>
</div>


## Overview

goya1746 is an overdrive & preamp pedal based on the legendary Diezel VH4 channel 3. Fully open circuit board designed in KiCad 8.  
The main idea was to avoid oscillations on all gain levels. Sharing this project is intended for hobbyists who want to study, modify, or build their own.  
The full PCB outline is 115 × 70 mm, but the usable area is about 96 × 70 mm if you remove the side "wings" in KiCad and define your own edge cut before generating Gerbers.


## Manufacturing

Check [Releases](https://github.com/escaroda/goya1746/releases) page for `.zip` Gerber files ready for production.
If you want to fabricate the PCB, just upload the `.zip` Gerber files to your favorite board house (e.g. JLCPCB, PCBWay, NEXTPCB).


## Important notes

- This pedal should be powered between 12-18VDC. Power draw 100mA. There are rumors 15VDC would give the best result, but our recommendation is 18VDC.
- The LM2940 regulator is installed vertically. Its metal tab can be mounted to the chassis to help dissipate heat — just make sure the chassis is grounded and not connected to any other signal paths. This workaround increases build complexity and will be refined in a future revision. The idea was to make the board as cool as possible.
- Only five electrolytic capacitors are used, and they are strategically placed to provide shielding for the TC1044SCPA charge pump switching regulator IC from nearby components.
- The resistor 2.2K 1/4W for the LED should be placed on the wire that connects it to the PCB.
- For reverse polarity protection, the 1N5817 Schottky diode should be soldered onto the + wire leading to the DC input. The striped end (cathode) faces the PCB. For example: DC Jack  →  [ Anode — Diode — Cathode ]  →  PCB. Make sure you understand where +V and Ground pins of DC Input are by looking at the PCB Design in KiCad.
- For experimental purposes, the mid-pot tone control is wired in the so-called "Marshall style," which gives the mid control a stronger effect and shifts the tone toward a punchier, more mid-rich sound compared to a "Fender style" tone stack. Future revisions may provide both options, allowing the choice to be independent of the PCB layout.
- Because of space limitations in this version, buffered bypass solder pads are not included. This may be added in a future revision. At the moment, the on/off switch must be wired as a true bypass by the builder.


P.S. – Future releases are not expected in the near term due to financial constraints. However, once the situation improves, development will continue, including projects such as Turbo Rat, SansAmp GT-2, Boss CE-2, as well as a search for the best fuzz circuit.


## Acknowledgments

- [Diezel](https://www.diezelamplification.com/) for inspiring design of modern high-gain amplifiers.
- [freestompboxes.org](https://www.freestompboxes.org/viewtopic.php?t=28011) and its wonderful community — without their prior work, this project would not have been possible.
- [PedalPCB](https://www.pedalpcb.com/product/valhalla/) DIY shop, for inspiration and for providing clear, easy-to-understand schematics.


## Bill of Materials Preview

|Reference          |Value           |Qty|
|-------------------|----------------|---|
|BASS1              |A1M             |1  |
|C1,C7,C15,C16      |22n             |4  |
|C2,C6,C13          |100p            |3  |
|C3,C4,C5,C17       |1u              |4  |
|C8,C23             |2n2             |2  |
|C9,C12,C18         |2u2             |3  |
|C10                |47p             |1  |
|C11                |4n7             |1  |
|C14                |560p            |1  |
|C19                |330n            |1  |
|C20,C22            |10u             |2  |
|C21                |1n              |1  |
|C24,C25,C26,C27,C28|47u             |5  |
|D1,D2,D5,D6        |1N4148          |4  |
|D3,D4              |1N4734A         |2  |
|D7                 |LED 12V         |1  |
|DEEP1,PRES1        |C25K            |2  |
|GAIN1              |A250K           |1  |
|IC4                |LM2940CT-12_NOPB|1  |
|IC100              |TC1044SCPA      |1  |
|J1                 |GUITAR INPUT    |1  |
|J2                 |DC INPUT        |1  |
|J3                 |POWER OUT       |1  |
|J4                 |GUITAR OUT      |1  |
|MID1               |B25K            |1  |
|R1                 |FerriteBead     |1  |
|R2,R3,R14          |1M              |3  |
|R4,R5,R15,R25,R37  |100K            |5  |
|R6,R13,R18,R33     |10K             |4  |
|R7,R10,R11,R17,R19 |220K            |5  |
|R8,R16             |470K            |2  |
|R9                 |680K            |1  |
|R20                |39K             |1  |
|R24                |1M5             |1  |
|R26,R34            |1K              |2  |
|R28                |100R            |1  |
|R30                |47R             |1  |
|R31                |56K             |1  |
|R32                |4K7             |1  |
|R36                |150K            |1  |
|R38,R39            |10R             |2  |
|TREBLE1            |B250K           |1  |
|U1                 |OPA2134         |1  |
|U2,U3              |TL072           |2  |
|VOL1               |A10K            |1  |


### PCB Specifications

- Layers: 2
- Thickness: 1.6 mm
- PCB Size: 115 x 70 mm
- Copper weight: 1 oz (default PCB fab)
- Trace clearance: 6 mil or 0.1524mm
- Soldermask: [Black / Green / Anything]
- Silkscreen: [White]
- Surface finish: HASL
- Material: FR-4
- Via finish: Tented
- Min. Drill Hole: 0.3 mm
- Assembly: Through-hole components only (no SMD)


### Recommended Fabricators
- NEXTPCB
- JLCPCB
- PCBWay


## Gallery

![3D View Front Clean](docs/goya1746_render_front_clean.jpg)
![3D View Front](docs/goya1746_render.jpg)
![3D View Back](docs/goya1746_render_back.jpg)

![PCB](docs/goya1746_pcb_quicklook.png)


## License

This hardware design is distributed under the MIT License.
Copyright (c) 2025 Dmitry Escaroda.


## Contribution

If you build this pedal, feel free to share photos or mods via Discussions.

