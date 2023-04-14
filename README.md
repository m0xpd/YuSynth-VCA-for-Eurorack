# YuSynth-VCA-for-Eurorack

**A Eurorack Version of Yves Usson's 'Simple VCA'**

This repository contains design files for my Eurorack version of Yves Usson's 'Simple VCA' circuit:
http://yusynth.net/Modular/EN/VCA/index.html

which has been described in a stripboard implemementation on Eddy Bergman's Synth DIY site:
https://www.eddybergman.com/2020/04/synthesizer-build-part-29-vca-yusynth_25.html

Yves (and Eddy) describe how the circuit can be constructed in a.c. or d.c. coupled versions; the d.c. coupled version (which should use LINEAR 'B'
potentiometers) is useful for handling CV signals, whereas the a.c. coupled version (which should use LOGARTHMIC 'A' potentiometers) is the standard
version for handling audio signals.

This Eurorack version is implemented on a single PCB, following closely Yves' original schematic. 

I have replaced the specified BC547 transistors with 2n3904s, as these are my everyday 'popcorn' NPNs. Yves does note this as a standard replacement 
and warns that the pinouts of the two transistors is revesed; 'CBE' becomes 'EBC'. 

My PCB is designed and silkscreened for 2n3904s, so if you want to swap back to the original BC547Cs, you'll have to put these in 'in reverse' 
(with the flat face of the case aligned with the curve on the silkscreen).

I have also swapped the two IC packages (a TL072 and a LM741/TL071) for a single TL074 for two reasons:
Firstly, it is more efficient in terms of PCB area to do this.
Secondly, it is cheaper to do this; TL074s are so widely used that they are cheap, whereas TL072s are rather less widespread, so they're relatively 
more expensive and TL071s are ridiculously, disproportionately expensive. Even more perversely, the old LM or uA741 (which was once the only op-amp 
in the shop) is now available only as a nostalgia piece, so it too sells for crazy money!

Having done this, I couldn't bear to have that extra op-amp doing nothing, so I gave both outputs independent active drivers.

The unpopulated board is shown below:

![Unpopulated PCB](https://user-images.githubusercontent.com/3152962/232078671-f9c0ce15-e9e0-4985-b357-16a027e5c78b.png)

The board hosts all the controls and sockets and is designed to fit to a front panel to make a complete 8HP module. 
The populated PCB is seen mounted on the front panel below:

![m0xpd VCA](https://user-images.githubusercontent.com/3152962/232079387-0153d039-fb5f-40cc-bcfa-8a5471c5c308.png)

**Licensing the IP**

Yves is clear on his website that:
"All circuits, schematics, printed circuit board, panel design and associated data published on (yusynth.net) can be used for private use only." 
and that:
"The projects of this site may be build for personal, private usage or educative purpose. Commercial exploitation of the schematics, circuits, front panels and software shown on (yusynth.net), is not permitted without a formal agreement with (Yves Usson)".

Accordingly, the copyright for the circuit rests with Yves and no commercial exploitation is permitted.

I have reflected this in the [License](License.txt) for the Eurorack version presented in this repository.



This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg

**Hardware Design Files: PCB**

The PCB is described by Eagle files .sch and .brd located in the PCB folder. These can be loaded into the (free) version of Eagle:
https://www.autodesk.co.uk/products/eagle/features
and are ready for the CAM processor to produce Gerber files ready to send to a PCB fabrication facilities. 

I have used JLCPCB (https://jlcpcb.com/) to produce the prototype seen in the pictures above (usual disclaimer). 
JLCPCB offer a file to set up the CAM processor to produce the Gerbers in the correct format - it is available (along with some guidelines) here:
https://support.jlcpcb.com/article/137-how-to-generate-gerber-and-drill-files-in-autodesk-eagle

I'm sure the other PCB houses offer an equivalent service - but I can't speak from first-hand experience.

**Hardware Design Files : Front Panel**

A front panel to complete the module is described by a simple Kicad project located in the Front_Panel folder. This contains files for a simple Kicad project, which defines the panel - you may wish eitehr to create your own or modify my design to 'personalise' it.

The process of Gerber and drill file generation in Kicad is a little more clunky than in Eagle, but you'll find on-line tutorials of how to do it.

**SetUp / Calibration**

Yves offers a useful description of setup on http://yusynth.net/Modular/EN/VCA/index.html, which assumes the availability of an oscilloscope. 
I imagine the circuit could be setup adequately without a 'scope - but I've never tried to do it! Certainly an a.c. coupled build of this VCA
could be made to work adequately without access to a 'scope in the setup phase, but I think it would be tricky to setup a d.c. coupled version without access 
to appropriate test gear.

