# Penta Five
A RISC-V vector processor written in Chisel HDL.

This repository contains all sources files for the project.
The processor was designed and implemented by Ulrik Helk and Mads Rumle Nordstroem.

This project asumes a unix like OS and basic development tools installed. 
Verilator is needed to run simulations.

Before generating verilog a program file needs to exist in the top directory of the project.
It should be called program.txt and it should contain a program written in pure hex machine code.
The following is an example a program that blinks a I/O port:
```
00000893 
02100513 
00000593 
00a5d663 
00158593 
ff9ff06f 
000028f3 
00000013 
00000013 
00000013 
0018c893 
00000013 
00000013 
00000013 
00089073 
fc5ff06f
```

To generate verilog do:
```
make run
```

To run a simulation do:
```
make test
```

To quicly see waveforms from simulation do:
```
make wave
```
or simulate and waveforms in one command:
```
make test wave
```

More options for configuring make targets can be specified in a config.mk file.


