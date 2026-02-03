# EDO_DRAM_CONTROLLER

This is a Verilog FSM for performing a march test on an EDO DRAM Memory. This initial design is very crude and needs to be reworked.

The design uses the FPGA as a memory controller which handles addressing, data reads and writes, and cell refreshes. 
Upon reading a word, the FPGA's data port becomes high impedance and a separate READ_TRIGGER pin signals a separate microcontroller to read the bus.
This implementation was done due to a lack of resources and is insufficient. 
Later updates should simplify the FSM and integrate a UART transceiver so the FPGA may handle reading memory and relaying this to the PC itself.

The DRAM memory has setup and timing characteristics that must be enforced. The timing constructs should be handled more cleanly in the future.
