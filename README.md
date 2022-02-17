# Register-File
32 bit Register File.
Includes 4 modules, one for a register that stores 32 bits of data, one for a 5bit decoder, one for a 32:1 multiplexer, and a top level file called registerFile that combines all of the other modules to create a 32 bit register of 32 bit width.

The registerFile specifically consists of 32 Individual Registers that can store 32 bits of data each, two multiplexers that can read the data from a specified register, and a decoder that can be used together with a write bit to write 32 bits of data in to a specific register. 

*Important* : Prior to running muxTB, a small change must be made to the mux file. The number of bits of the input on line 4 and the output reg on line 8 should be changed from 32 bits to 8 bits (from [31:0] to [7:0]). The test bench was made to run using 8 bits instead of 32 because the main file would not compile using 32 bits due to size.
