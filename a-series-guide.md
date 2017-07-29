---
title: TinyFPGA A-Series User Guide
---

## Getting Started
The TinyFPGA A-Series boards use Lattice Semiconductor's MachXO2 FPGAs.  

### Hardware
Of course you will need to purchase one or more A-Series boards, but you will also need a few other things to get working.
1. TinyFPGA [A1](http://store.tinyfpga.com/product/tinyfpga-a1) or [A2](http://store.tinyfpga.com/product/tinyfpga-a2) Board.
2. [Pins](http://store.tinyfpga.com/product/a-series-pins) if you want to solder the board to another PCB, insert it into a socket, or use with a solderless breadboard.
3. 3.3 volt power supply.  You can use a [3.3 volt regulator](http://store.tinyfpga.com/product/a-series-3-3-volt-regulator-ld1117v33), a lab power supply, or use an existing 3.3 volt power supply from your project.
4. [JTAG programmer](https://www.ebay.com/sch/i.html?_nkw=lattice+fpga+jtag).  TinyFPGA currently doesn't have a JTAG programmer, but I hope to soon have an opensource Arduino sketch available soon and very low-cost programmer hardware later.
5. [Something](https://www.google.com/search?q=godzilla+robot&safe=active&tbm=isch) [interesting](https://www.google.com/search?q=quad+copter&safe=active&tbm=isch) [to](https://www.google.com/search?q=3d+printer+open+source&safe=active&tbm=isch) [control](https://www.google.com/search?q=vga+graphics&safe=active&tbm=isch) [or](https://www.google.com/search?q=retro+console&safe=active&tbm=isch) [interface](https://www.google.com/search?q=retro+computer&safe=active&tbm=isch) [with](https://www.google.com/search?q=tcp+ip&safe=active&tbm=isch).  If you are just starting out you could use some LEDs or maybe a logic analyzer.  Otherwise you might have something more specific in mind ;)

### Software
You will need to install the latest development environment and other support tools for the MachXO2 FPGAs and the A-Series boards.

1. Download and install [Lattice Diamond](http://www.latticesemi.com/latticediamond).  It is available for both [Windows](http://www.latticesemi.com/latticediamond#windows) and [Linux](http://www.latticesemi.com/latticediamond#linux).
2. [Request a free license file](http://www.latticesemi.com/Support/Licensing/DiamondAndiCEcube2SoftwareLicensing/DiamondFree.aspx) in order to use the [Lattice Diamond](http://www.latticesemi.com/latticediamond) software.
3. The TinyFPGA A-Series GitHub Repository has Lattice Diamond template projects that you may find useful.  They include an empty top-level verilog module with pin constraints to map board pins to the correct IOs on the MachXO2 FPGA chip.  You could [download the latest files directly in a zip file](https://github.com/tinyfpga/TinyFPGA-A-Series/archive/master.zip) or [clone the repo using git](https://github.com/tinyfpga/TinyFPGA-A-Series.git).
