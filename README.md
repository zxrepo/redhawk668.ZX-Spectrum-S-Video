# Introduction

This PCB replaces the RF modulatorbox on a Sinclair ZX Spectrum computer. It's main purpose is to improve the video output of the ZX Spectrum by seperating the luma/sync (Y) and chroma (C) signals.

The ZX Spectrum does have a composite signal that goes into the modulatorbox, a simple modification is to cut off the +5 volt to the modulator, disconnect the composite signal from the RF modulator and feed the signal to the RCA jack of the modulator. This results in a signal that is slightly better than RF. This is a common mod and is easy to perform. However, the image has a lot of dot crawl, because the pixel clock is not synchronised with the PAL colour subcarrier.

# Composite output works, why designing this board?
Why not? I use a RetroTink 2X (https://www.retrotink.com/product-page/retrotink-2x), this little device converts an analog signal to HDMI output. The Spectrum's composite output is absolutely horrible on this. The RetroTink provides an s-video input, that gave me the idea to seperate the Y/C signals to convert the composite output to s-video, improving the video signal. Some googling later I found this thread on the World of Spectrum forums: 

https://www.worldofspectrum.org/forums/discussion/47120/new-video-about-s-video-modification-on-issue-two-48k-spectrum/p1. 

Credits to MAK1024 and RGA24 for providing the basics for this design.

I first built it up on a piece of stripboard and did some testing and it worked quite well with my RetroTink. A nice clear picture without dot crawl. It also gives a good picture on a Commodore 1701 CRT. 

This PCB makes the modification a bit easier to carry out and it is reversible. 

# The PCB itself

# Rev. A
![alt text](https://github.com/redhawk668/ZX-Spectrum-S-Video/blob/master/Rev.%20A/Final%20Design.png)

# Rev. B
![alt text](https://github.com/redhawk668/ZX-Spectrum-S-Video/blob/master/Rev.%20B/Final%20Design%20Rev.%20B%20-%20Red.png)

Rev. A is the first design I made and is a through hole design. Rev. B is the second I made and this a fully SMD design and based on an FMS6143 video filter driver.

I have included the Gerber files from both designs, so you can have the PCB of your choice manufactured by your preferred manufacturer.

# Billing of Materials: Rev. A
- 1x 4 pin mini din chassis (Lumberg TM 0508 A/4)
- 3x NPN Transistors. I've used BC547, but most small signal transistors should be fine.
- 1x 2K2 Resistor
- 1x 3K9 or 1x 4K3 Resistor
- 1x 390R Resistor
- 1x 22uF Electrolytic Capacitor
- Some wire
- 2x M2.5 screws
- 4x M2.5 nuts

# Billing of Materials: Rev. B
- 1x 4 pin mini din chassis (Lumberg TM 0508 A/4)
- Q1: BC847, SOT23
- C1: 0,1 uF ceramic capacitor XR7, 0805
- C2: 0,1 uF ceramic capacitor XR7, 0805
- C3: 0,1 uF ceramic capacitor XR7, 0805
- C4: 1 uF aluminium electrolytic capacitor (4x5,3)
- C65: 22 uF aluminium electrolytic capacitor (6,3x5,3)
- R1: 2K2 thick film resistor, 0805
- R2: 4K3 thick film resistor, 0805
- R3: 390R thick film resistor, 0805
- R4: 75R thick film resistor, 0805
- R5: 75R thick film resistor, 0805
- Some wire
- 2x M2.5 screws
- 4x M2.5 nuts

# Summary
Once you have built the little circuit, solder in wires for luma in, chroma in and +5 volt in. Make the wires for luma in and +5 volt about 50mm. PCB layout on an Issue 2 is a bit different than Issue 3 and above. 50mm for the chroma wire should be long enough for an Issue 2. Issue 3 and above needs a bit longer wire. 

![alt text](https://github.com/redhawk668/ZX-Spectrum-S-Video/blob/master/IMG_20200522_165732.jpg)

Now, remove the modulatorbox and capacitor C65 from the Spectrum PCB. Now carefully mount the PCB onto the Spectrum PCB using the screws and nuts (might need drilling, but M2.5 should fit). Seperate the PCB's using one of the nuts on either side. Tighten the PCB to the Spectrum PCB using a nut on either side, as shown in the picture:

![alt text](https://github.com/redhawk668/ZX-Spectrum-S-Video/blob/master/IMG_20200522_165952.jpg)

Now solder the luma and +5 volt to their respective holes. (The composite output on the Spectrum is now the luma output). Solder the chroma wire to the pad for the + side of capacitor C65. On Issue 2 PCB's C65 is underneath the modulator box, on Issue 3 boards and above, C65 is above C25 on the left side of the PCB.

# Issue 2:

![alt text](https://github.com/redhawk668/ZX-Spectrum-S-Video/blob/master/IMG_20200524_162537.jpg)

# Issue 3 and above:

![alt text](https://github.com/redhawk668/ZX-Spectrum-S-Video/blob/master/IMG_20200522_165732.jpg)

I recommend cutting the pins of the mini din chassis as close to the underside of the PCB as possible, to prevent short circuits. 

# Disclaimer
I am not responsible for any damage to your Spectrum, you do this at your own risk. Take care when you build this and when fitting it to your Spectrum.


























