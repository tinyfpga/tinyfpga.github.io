---
title: TinyFPGA
---

The TinyFPGA boards are a new series of low-cost, [open-source](https://github.com/tinyfpga) FPGA boards in a tiny form factor.  Solder on pins for use in a breadboard or PCB socket; or solder connectors, wires, and components directly onto the board.

## TinyFPGA Boards

|                                   | [TinyFPGA A1](https://store.tinyfpga.com/products/tinyfpga-a1) | [TinyFPGA AX2](https://store.tinyfpga.com/products/tinyfpga-a2) | [TinyFPGA BX](https://www.crowdsupply.com/tinyfpga/tinyfpga-bx) | TinyFPGA EX |
|-----------------------------------|:-----------:|:-----------:|:-----------:|:-----------:|
|                                   |[![](a1-thumb.jpg)](https://store.tinyfpga.com/products/tinyfpga-a1)|[![](a2-thumb.jpg)](https://store.tinyfpga.com/products/tinyfpga-a2)|[![](TinyFPGA-BX.png)](https://www.crowdsupply.com/tinyfpga/tinyfpga-bx)|![](TinyFPGA-EX.png)|
| FPGA Chip                         |   XO2-256   |   XO2-1200  |  ICE40LP8K  | LFE5U-25F  |
| Programming Interface             |     JTAG    |     JTAG    |     USB     |    USB     |
| Logic Cells                       |     256     |     1200    |     7680    |   24288    |
| Distributed RAM                   |    2 KBit   |   10 KBit   |             |   194 KBit |
| Block RAM                         |             |   64 KBit   |   128 KBit  |  1008 KBit |
| User Flash                        |             |   64 KBit   |  6000 KBit  | 96000 KBit |
| Phase Lock Loops                  |             |      1      |      1      |     2      |  
| Delay Lock Loops                  |             |             |             |     2      |  
| User IO Pins (dedicated + shared) |    18 + 4   |    18 + 4   |   31 + 10   |   49 + 7   |
| Price                 |[$12](https://store.tinyfpga.com/products/tinyfpga-a1)|[$18](https://store.tinyfpga.com/products/tinyfpga-a2)|[$38](https://www.crowdsupply.com/tinyfpga/tinyfpga-bx)|   

## TinyFPGA in the News
* **EEWeb.com**
  * [A Look at TinyFPGA Boards](https://www.eeweb.com/profile/duane-benson-2/articles/a-look-at-tinyfpga-boards)
  * [Grinding Coffee with a TinyFPGA Board](https://www.eeweb.com/profile/duane-benson-2/articles/grinding-coffee-with-a-tinyfpga-board)
* **Hackster.io**
  * [The Next Generation of TinyFPGAs](https://blog.hackster.io/the-next-generation-of-tinyfpgas-722742afe783)
  * [The Coming of the Age of the Maker FPGA Board](https://blog.hackster.io/the-coming-of-the-age-of-the-maker-fpga-board-52a29572549e)
* **Hackaday.com**
  * [TinyFPGA is a Tiny FPGA Board](https://hackaday.com/2017/07/31/tinyfpga-is-a-tiny-fpga-board/)
  * [Hackaday Prize Entry: Programming FPGAs with Themselves](https://hackaday.com/2017/10/23/hackaday-prize-entry-programming-fpgas-with-themselves/)
* **CNXSoft - Embedded Systems News**
  * [TinyFPGA is a Breakout Board for Lattice Semi MachXO2 FPGA](https://www.cnx-software.com/2017/07/24/tinyfpga-is-a-breakout-board-for-lattice-semi-machxo2-fpga/)
  
**[Customer Reviews](https://www.tindie.com/stores/tinyfpga/reviews/)**
  
## Buy with Shipping from USA
<a href="http://store.tinyfpga.com"><img src="TinyFPGA-Logo.png" alt="TinyFPGA Store" /></a>

<a href="https://www.crowdsupply.com/tinyfpga"><img src="crowd-supply-logo-dark.png" alt="Crowd Supply" /></a>

<a href="https://www.tindie.com/stores/tinyfpga/"><img src="https://d2ss6ovg47m0r5.cloudfront.net/images/tindie-logo@2x.png" alt="Tindie" /></a>

## Buy with Shipping from Europe
<a href="https://www.elektor.com/search?q=tinyfpga"><img src="https://www.elektor.com/skin/frontend/default/elektor/images/logo.gif" alt="Elektor" /></a>

## User Guides
The A- and B-Series boards use different FPGA families and their toolchains are different.  See the below guides to learn how to get started.

### [A-Series Guide](a-series-guide.html)

### B-Series Guides
#### [BX Guide](bx/guide.html)
#### [B2 Guide](b-series-guide.html)

## FPGA Tutorials

I am developing a regular series of tutorials, articles, and hands-on labs utilizing the TinyFPGA boards.  They can be found on hackaday.io: [The Hobbyist's Guide to FPGAs](https://hackaday.io/project/27550-the-hobbyists-guide-to-fpgas).  If you are new to FPGAs and want to give them a try, this guide is for you.  If you haven't already, sign up for hackaday.io and follow the project to be notified when there are updates.

## TinyFPGA Discourse Community

A brand new Discourse server has been setup for TinyFPGA.  If you are interested in the TinyFPGA boards, join the [TinyFPGA Discourse](http://discourse.tinyfpga.com/) and ask away.  Luke is there often to help troubleshoot problems, answer questions, and post news.  Over time this will grow into the best place to meet other hobbyists, makers, and professionals interested in FPGAs and the TinyFPGA project.

## Digital Design Tools
### A-Series
The A-series boards use the [Lattice Diamond](http://www.latticesemi.com/latticediamond) design software for synthesizing digital designs into FPGA bitstreams.  It can be downloaded for free from [Lattice Semiconductor's website](http://www.latticesemi.com/latticediamond).  Follow their instructions carefully to get a free license file.

### B-Series
The B-series boards use the open source [Project IceStorm](http://www.clifford.at/icestorm/) tools or [Lattice iCEcube2](http://www.latticesemi.com/iCEcube2) design software for synthesizing digital designs into FPGA bitstreams.  Just like Lattice Diamond, iCEcube2 requires a free license file to be downloaded so be sure to follow their directions carefully.  The open source IceStore toolchain needs no special license.

To jumpstart development simple [iCEcube2 project template](https://github.com/tinyfpga/TinyFPGA-B-Series/tree/master/icecube2_template) and [IceStorm project template](https://github.com/tinyfpga/TinyFPGA-B-Series/tree/master/icestorm_template) projects are provided with top-level verilog files that represent the pins on the B-series boards.  These projects contain a timing constraint for the 16MHz clock and pin constraints for each of the pins.  You can download the template as part of the [TinyFPGA B-Series Repository ZIP](https://github.com/tinyfpga/TinyFPGA-B-series/archive/master.zip).

## FPGA Programmer
### A-Series
The A-series boards are programmed via JTAG.  There is a dedicated [TinyFPGA Programmer](http://store.tinyfpga.com/product/tinyfpga-programmer) available to purchase.  It is the most cost-effective and convenient programmer for the A-series boards.  It can be used with the [TinyFPGA Programmer Application](https://github.com/tinyfpga/TinyFPGA-Programmer-Application/releases).

You can also use Lattice-compatible JTAG programmers [JTAG Programmer Hardware](https://www.ebay.com/sch/i.html?_productid=533163279) and the [Lattice Programmer Software](http://www.latticesemi.com/programmer).  

### B-Series
The B-series boards have a built-in USB bootloader.  To program a bitstream use the [TinyFPGA B-Series Programmer](https://github.com/tinyfpga/TinyFPGA-Programmer-Application/releases/) and select the serial port of the device and bitstream file.  If you are using Linux or OSX you can run the programmer application as a Python script.  It is available in the [TinyFPGA B-Series GitHub Repo](https://github.com/tinyfpga/TinyFPGA-B-Series/tree/master/programmer). You can download the programmer python scripts as part of the [TinyFPGA B-Series Repository ZIP](https://github.com/tinyfpga/TinyFPGA-B-Series/archive/master.zip).

![](b-programmer.png)

## Contact Information
```
email: luke@tinyfpga.com

Luke Valenty
TinyFPGA
1750 Prairie City Rd
Suite 130 #751
Folsom, CA 95630
```




