[This folder](https://github.com/m0xpd/YuSynth-VCA-for-Eurorack/tree/main/PCB) contains design files for the Eurocard version of the YuSynth VCA printed circuit board developed in AutoCAD EAGLE.

These can be loaded into the (free) version of Eagle:
https://www.autodesk.co.uk/products/eagle/features
and are ready for the CAM processor to produce Gerber files ready to send to a PCB house. 

I have used JLCPCB (https://jlcpcb.com/) to produce the prototype seen in the pictures below (usual disclaimer). 
JLCPCB offer a file to set up the CAM processor to produce the Gerbers in the correct format - it is available (along with some guidelines) here:
https://support.jlcpcb.com/article/137-how-to-generate-gerber-and-drill-files-in-autodesk-eagle

I'm sure the other PCB houses offer an equivalent service - but I can't speak from first-hand experience.

The unpopulated board is seen here:

![Unpopulated PCB](https://user-images.githubusercontent.com/3152962/232187698-64415e3e-4dcb-4a7e-969c-389b76491eb7.png)

and the populated board is seen here (both from the 'front side', usually obscured by the front panel and from the back):

![Populated PCB](https://user-images.githubusercontent.com/3152962/232188158-9b3b2cb8-2b80-437d-991e-02d6b0e7ab3c.png)

**Bill of Materials**

The BoM is presented in the rather verbose format produced by eagle; some additional notes might be useful.

Firstly, Yves explains that two versions of the VCA can be constructed: an a.c. coupled version (for handling 'audio' signals) and a d.c. version 
(useful for controlling CV signals).

The a.c. coupled version is the standard build. It uses all the parts in the BoM. The three 100k control potentiometers should be logarithmic 
taper types in this application, 'A100K'. Linear taper potentiometers will work in this application, but they will give the usual poor mapping 
between rotational angle and 'loudness'. Note that these are named with idents 'SIGLEVEL','GAIN', and 'CTLLEVEL' (Yves uses the idents 'P1', P2' 
and P3').

The d.c. coupled version is non-standard. To make the system d.c. coupled, capacitors C3 and C4 must be replaced by wire links. Also, the signal 
level monitor will not operate as intended and should be omitted (do not fit R 24&25, C8&9 D1, LED1 and T4). In this case, the three control
potentiometers should be linear, 'B100K'.

I've made both versions.

The control potentiometers in my design are 9mm vertical Alpha types such as [this](https://www.thonk.co.uk/shop/alpha-9mm-pots-vertical-t18/) and 
the jacks are [Thonkiconns](https://www.thonk.co.uk/shop/thonkiconn/).

Back in the day I used 3-way Molex KK connectors for powering modules and I still fit these as an alternative to the standard Eurorack power 
connector if spaces is available - you can omit this 'POWER' header if you don't want to use it!
