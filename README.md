# Testing build system environments for FPGA
Project to test different build system environments for FPGA.

* Possibilities to explore:
  * hdlmake
  * cmake
* Tools:
  * open source
    * ghdl (included in hdltools)
    * yosys (included in hdltools)
    * openFPGA (TODO: include in hdltools?)
    * gtkwave (included in hdltools)
    * netlist2svg (https://github.com/nturley/netlistsvg ; included in hdltools)
    * vcd2png (https://github.com/naelolaiz/hdltools/blob/main/vcd2png.py)
    * gtkwavexport (https://github.com/naelolaiz/learning_fpga/blob/main/scripts/gtkwave_export.py; vcd2png.py in hdltools)
  * ...
  * multisim?

# Definition of the project
 - The idea is to use a simple project (a blinking LED at first, at the end I can test more involved code, as defining and using ROM blocks...) to test different approaches for build systems for FPGA.
 - Use container with all required (open-source) tools (ghcr.io/naelolaiz/hdltools:release)
  - Every implementation should include synthesis with mixed code (vhdl, verilog, ...), and simulation. 
    - This should be exercised on github actions.
    - Ideally, it should be also able to generate a bitstream for at least a Cyclone IV and Zybo boards I own, and publish them as artifacts of the CI actions.
    - Extend to use gtkwave to publish simulation graphics
    - Use yosis+netlist2svg to generate logic diagrams

* GHDL+yosys+gtkwave+netlist2svg previous experiments in github actions of:
  * https://github.com/naelolaiz/fpga_tutorial
  * https://github.com/naelolaiz/learning_fpga
* hdlmake + multisim github action example:
  * https://github.com/hdl-util/hdmi
