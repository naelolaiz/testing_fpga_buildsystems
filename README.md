Project to test different build system environments for FPGA.

Possibilities to explore:
 * hdlmake
 * cmake
Tools:
 * ghdl
 * yosys
 * openFPGA
 * ...
 * multisim?


The idea is to use a simple project (a blinking LED at first, at the end I can test more involved code, as defining and using ROM blocks...) to test different approaches for build systems for FPGA.
Every implementation should include synthesis with mixed code (vhdl, verilog, ...), and simulation. This should be exercised on github actions.
Ideally, it should be also able to generate a bitstream for at least a Cyclone IV and Zybo boards I own, and publish them as artifacts of.

