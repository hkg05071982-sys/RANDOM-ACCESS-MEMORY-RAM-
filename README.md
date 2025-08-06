1. # RANDOM-ACCESS-MEMORY-RAM-

RAM is a type of volatile computer memory that allows data to be read from and written to in any order (random access) with equal speed. It is used as the main memory in computers and digital systems to temporarily store data and instructions that the CPU needs during operation.

2. Applications:-

Main memory in computers, smartphones, and embedded systems.

Buffers and caches in hardware.

Temporary storage for active applications and processes.

3. Overview:-

This project implements a parameterized Random Access Memory (RAM) in Verilog with:

1 write port (synchronous)

1 read port (synchronous)

4. Parameterizable data width and address width

| Parameter | Description                              | Default |
| --------- | ---------------------------------------- | ------- |
| `D_WIDTH` | Data width of each memory location       | 16      |
| `A_WIDTH` | Width of the address bus                 | 4       |
| `A_MAX`   | Number of memory locations (`2^A_WIDTH`) | 16      |

5. Testbench: test
   
Features:-

Instantiates the ram module with:

D_WIDTH = 8

A_WIDTH = 5

A_MAX = 32

Generates write and read clocks using tasks.

Demonstrates:

Reading initial data from a memory address.

Writing new data to the same address.

Reading back the updated data.

Dumps waveform data to dump.vcd for simulation

6:-Simulation:-

iverilog -o ram_tb.vvp ram.v test.v

vvp ram_tb.vvp

gtkwave dump.vcd

OUTPUT:-
<img width="1823" height="527" alt="Image" src="https://github.com/user-attachments/assets/3710231e-3c55-4ebf-82c5-1a1b3f818f60" />

