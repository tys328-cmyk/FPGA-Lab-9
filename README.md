ECE 128 Lab 9 – RAM and ROM Design

Project Description

This project implements two basic types of memory in Verilog: a RAM that reads and writes 8-bit data in 8 memory locations, and a ROM that stores 4-bit data in 8 memory locations. The RAM has an address, data input, write enable, and clock, and returns the data stored at the addressed location. The ROM has only an address input and returns the fixed data stored at the addressed location. The contents of both memories are handled through a text file using a Verilog file-reading system task such as $readmemh or $readmemb, so the stored data can be changed by editing the text file instead of the Verilog code. Each design has its own testbench, and the two designs are compared based on FPGA resource utilization.

Simulation

1. Open the project in Vivado.
2. Add the RAM or ROM module as a design source.
3. Add the text file containing the memory data to the project, and make sure the file path used in the Verilog code points to it.
4. Add the corresponding testbench as a simulation source.
5. Set the testbench as the simulation top module.
6. Run Behavioral Simulation.
7. Verify from the waveform that the data read from each address matches the expected contents. For the RAM, check that the data read back matches the data that was written and that the contents do not change when write enable is inactive. For the ROM, check that the output at each of the 8 addresses matches the value stored at that address in the text file.

FPGA Implementation

This lab is verified through simulation, and no FPGA programming is required. To view the resource usage of each design:

1. Select the Basys 3 as the target FPGA board.
2. Select the RAM or ROM module as the top module.
3. Run Synthesis.
4. Open the synthesized design and generate the Utilization Report to view the LUT, IOB, and clock buffer usage.
