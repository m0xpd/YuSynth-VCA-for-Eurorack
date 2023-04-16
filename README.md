# YuSynth-VCA-for-Eurorack

**A Eurorack Version of Yves Usson's 'Simple VCA'**


![Screenshot 2023-04-14 at 19 14 45](https://user-images.githubusercontent.com/3152962/232124759-e040d76c-e61c-4e8d-8a22-aa63c274c8ec.png)



This repository contains design files for my Eurorack version of Yves Usson's 'Simple VCA' circuit:
http://yusynth.net/Modular/EN/VCA/index.html

which has been described in a stripboard implemementation on Eddy Bergman's Synth DIY site:
https://www.eddybergman.com/2020/04/synthesizer-build-part-29-vca-yusynth_25.html



**Circuit Description**

This Eurorack version is implemented on a single PCB, following closely Yves' original schematic.<p>(You can see my schematic as a graphic [here](https://github.com/m0xpd/YuSynth-VCA-for-Eurorack/blob/main/PCB/YuSynth%20Eurorack%20VCA%20Schematic.png) and the BoM is [here](https://github.com/m0xpd/YuSynth-VCA-for-Eurorack/blob/main/PCB/YuSynth%20VCA%20Eurorack%20v1%20BOM.txt) )


I have replaced the specified BC547 transistors with 2n3904s, as these are my everyday 'popcorn' NPNs. Yves does note this as a standard replacement 
and warns that the pinouts of the two transistors is revesed; 'CBE' becomes 'EBC'. 

My PCB is designed and silkscreened for 2n3904s, so if you want to swap back to the original BC547Cs, you'll have to place these 'in reverse' 
(i.e. with the flat face of the case aligned with the curve on the silkscreen).

I have also swapped the two IC packages (a TL072 and a LM741/TL071) for a single TL074 for two reasons:
Firstly, it is more efficient in terms of PCB area to do this.
Secondly, it is cheaper to do this; TL074s are more efficient than their smaller siblings (they only need one pair of power supply pins) but they're 
also very widely used so they are cheap, whereas TL072s and (particularly) TL071s are disproportionately expensive. Even more perversely, the old LM 
or uA741 (which was once the only op-amp in the shop) is now available only as a nostalgia piece, so it too sells for crazy money!

Having done this, I couldn't bear to have that extra op-amp stage doing nothing, so I gave both outputs independent active drive.

  
  

**Licensing the IP**

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg  
  
Yves is clear on the position with copyright on his website:

"All circuits, schematics, printed circuit board, panel design and associated data published on (yusynth.net) can be used for private use only." 

and:

"The projects of (yusynth.net) may be build for personal, private usage or educative purpose. Commercial exploitation of the schematics, circuits, 
front panels and software shown on (yusynth.net), is not permitted without a formal agreement with (Yves Usson)".

Accordingly, **the copyright for this VCA circuit rests with Yves and no commercial exploitation is permitted**.

I have reflected this in the [License](LICENSE.txt) for the Eurorack version presented in this repository.

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

<p>

  
  
</p>

  
**Hardware Design Files: PCB**

The PCB is described by .sch and .brd files and a BoM located in the [PCB folder](https://github.com/m0xpd/YuSynth-VCA-for-Eurorack/tree/main/PCB). 

**Hardware Design Files : Front Panel**

A front panel to complete the module is described by a simple Kicad project located in the [Front_Panel folder](https://github.com/m0xpd/YuSynth-VCA-for-Eurorack/tree/main/Front_Panel). 

  
  
**SetUp / Calibration**

Yves offers a [useful description of setup](http://yusynth.net/Modular/EN/VCA/index.html), which assumes the availability of an oscilloscope. 
I imagine the circuit could be setup adequately without a 'scope - but I've never tried to do it! Certainly an a.c. coupled build of this VCA
could be made to work adequately without access to a 'scope in the setup phase, but I think it would be tricky to setup a d.c. coupled version without access 
to appropriate test gear.

