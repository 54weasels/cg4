# Sun CG/4
From [Frame Buffer History Lesson](https://www.sunhelp.org/faq/FrameBufferHistory.html):
```
cg4: device name: "/dev/cgfour0"  
```
Project name: Prism The dumb 8-bit color frame buffer with overlay and enable planes. Found in 3/110C, 3/60C, 4/110C and 4/150C. This is the first one using the "P4" bus.

The 10-bit deep frame buffer found on the CPU board of the Sun-3/110, and as an option to the Sun-3/60 and Sun-4/110. The 10 bits on the frame buffer are: 8-bits color frame buffer, 1 bit monochrome frame buffer and 1 bit enable plane, which determines which bits of the colour and mono planes are displayed.

For a Sun-4/110, Sun-3/60 and other machines with a P4 connector the CG4 frame buffer is a daughter-board. Note that no GP can be added to the CG4. There is no rasterop hardware on the CG4 frame buffer. The CG4 will "probably" be on all desktop P4 type products. The device driver for the CG4 is called "cgfour".

```
device cgfour0 at obmem 7 csr 0xff300000 priority 4  
```
This is the P4 bus color frame buffer for the 3/60 and 4/110

Resolution is **1152x900**
