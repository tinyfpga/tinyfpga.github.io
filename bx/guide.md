---
title: TinyFPGA BX User Guide
---

## Getting Started
The TinyFPGA BX boards use Lattice Semiconductor's iCE40 FPGAs.  There are a number of existing software and hardware tools available as well as documentation from Lattice for these FPGAs.  This guide will help get you started with the BX board, the tools, and documentation available for the FPGA chips themselves.

## Hardware
Of course you will need to purchase one or more BX, but you will also need a few other things to get working.

1. [TinyFPGA BX](https://www.crowdsupply.com/tinyfpga/tinyfpga-bx) Board.
2. Pins if you want to solder the board to another PCB, insert it into a socket, or use with a solderless breadboard.
3. [Something](https://www.google.com/search?q=godzilla+robot&safe=active&tbm=isch) [interesting](https://www.google.com/search?q=quad+copter&safe=active&tbm=isch) [to](https://www.google.com/search?q=3d+printer+open+source&safe=active&tbm=isch) [control](https://www.google.com/search?q=vga+graphics&safe=active&tbm=isch) [or](https://www.google.com/search?q=retro+console&safe=active&tbm=isch) [interface](https://www.google.com/search?q=retro+computer&safe=active&tbm=isch) [with](https://www.google.com/search?q=tcp+ip&safe=active&tbm=isch).  For this guide we will use the user/boot LED built into the board itself.

## Software
You will need to install the latest development environment and other support tools for the iCE40 FPGAs and the BX board.  The TinyFPGA BX is supported by completely open source tools.  These instructions should work for all platforms.

### 1. Download and install [Atom](https://atom.io/).

### 2. Install Python

#### Linux
Your Linux distribution should already have Python installed.

#### Windows
1. Download and run the [Windows Python Installer](https://www.python.org/ftp/python/3.6.5/python-3.6.5-amd64-webinstall.exe).
2. **Important:** Check the "Add Python 3.6 to PATH" checkbox.
3. Click on "Install Now"
4. When Python has finished installing, click "Close".

#### MacOS
1. Download and run the [MacOS Python Installer](https://www.python.org/ftp/python/3.6.5/python-3.6.5-macosx10.6.pkg).
2. 

### 3. Install the APIO-IDE package for Atom.

### 4. Install APIO



## First Project Tutorial

Once you have all of your hardware and software ready you can get started developing some digital logic.  This first project won't go into all the details of designing and implementing digital logic circuits in general, but it will guide you through the specifics of setting up a simple project, writing verilog, and programming the board with the project. 

### 1. Connect USB cable

Connect a micro USB cable to the TinyFPGA board.  Use a quality cable to minimize programming issues.  The power LED should light up when the board is connected.  The boot LED should pulse on and off to indicate the bootloader is active.

### 2. Copy the template project from the [TinyFPGA BX Repository](https://github.com/tinyfpga/TinyFPGA-BX/archive/master.zip)

Copy the [`apio_template`](https://github.com/tinyfpga/TinyFPGA-BX/tree/master/apio_template) directory to a new directory and rename it `blink_project`.

### 3. Open your newly copied template project

Open the Lattice iCEcube2 application.  From the `File` menu select `Open` and `Project...`.  In the newly opened file chooser, navigate to the `blink_project_b` directory you just created and select the `template_sbt.project` project file.

![](lattice-icecube2-select-project.png)

### 4. Program the FPGA board

* In Windows, open the 'TinyFPGA Programmer' application via the start menu.
* In MacOS and Linux, open the `TinyFPGA Programmer` application by running the `tinyfpgab-programmer.py` python module from the [TinyFPGA Programmer Application GitHub Repo](https://github.com/tinyfpga/TinyFPGA-Programmer-Application/releases/).

The bootloader on the B-Series boards will present itself as a serial port.  The programmer application will display serial port identifiers for each TinyFPGA board it can program.

When you first connect a B-Series board it may not be immediately ready to program.

![](b-series-bootloader-not-active.png)

If this happens you can press the reset button on the B-Series board to active the bootloader bitstream.  Once the bootloader is active the programmer application status will update.

![](b-series-bootloader-active.png)

Select the bitstream to program.  This will be buried a few directories under the project: `template_Implmnt/sbt/outputs/bitmap/TinyFPGA_B_bitmap.hex`

If you're using IceStorm for synthesis the bitstream will be a `.bin` file in the same directory as your project:
`icestorm_template/TinyFPGA_B.bin`

![](b-series-ready-to-program.png)

Press the `Program FPGA` button to program the bitstream to the user area of the FPGA board SPI flash.  The programmer application will keep you updated with the status.  If it fails, press the reset button and try again.  If the application becomes unresponsive, close the application, unplug the FPGA board, and start over.  If you have trouble programming your TinyFPGA B-Series board please contact me for help at luke@tinyfpga.com.

The programmer application will verify the bitstream was written correctly and report 'Success!' if all is well.  The programmer should also report that the bootloader is not active.  This is because the bootloader does not consume any FPGA resources while the user configuration is running.  The bootloader can be enabled again by pressing the reset button on the TinyFPGA board.

![](b-series-programmed-running.png)

### 9. Verify the design works on the board as intended

If everything is working as it should, you should see the user LED on the board blinking a "SOS" in morse code.  

If you see the LEDs blinking congratulations!  You've successfully programmed your open hardware FPGA board with open source tools.  If you are familiar with Verilog and digital design you are ready to implement more complicated designs on your board(s).

![](tinyfpga-b-blinky.jpg)

## Extra Resources
* [TinyFPGA BX Repository](https://github.com/tinyfpga/TinyFPGA-BX)
* [TinyFPGA B-Series Project on Hackaday.io](https://hackaday.io/project/26848-tinyfpga-b-series)
* Generic FPGA and Verilog Tutorials
  * [http://www.fpga4fun.com/](http://www.fpga4fun.com/)
  * [Digital Logic Tutorial](http://www.asic-world.com/digital/tutorial.html)
  * [Verilog Tutorial](http://www.asic-world.com/verilog/veritut.html)
* [Lattice iCE40 Page](http://www.latticesemi.com/Products/FPGAandCPLD/iCE40.aspx)
  * [iCE40 LP/HX Family Data Sheet](http://www.latticesemi.com/view_document?document_id=49312)
  * [iCE40 sysCLOCK PLL Design and Usage Guide](http://www.latticesemi.com/view_document?document_id=47778)
  * [Memory Usage Guide for iCE40 Devices](http://www.latticesemi.com/view_document?document_id=47775)
