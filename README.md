# DA_FIR
Distributed Arithmetic based FIR-Filter and its VHDL-Code Generation with MATLAB Livescript
## Introduction
This project is the design and implementation of algorithms for FIR filters and convolutional operations on Xilinx FPGAs using VHDL, which mainly using cascaded MUX-optimised distributed arithmetic and automated VHDL code generation with MATLAB Livescript.

## Environment  
This project is developed on windows, theoretically compatible for linux
  - Hardware
    - Xilinx Zynq-7010clg400-1
  - Vivado 2022.1 or higher  
  - MATLAB R2022a or higher
    - Filter Design HDL Coder
    - Fixed-Point Designer
    - Signal Processing Toolbox
    - Support for MinGW-w64 C/C++ Compiler

## File structure
  - VHDL_Code:
    - includes all VHDL code for the DA algorithm
    - Naming format `FIR_DA_[var1]L_[var2]M.vhd`
    - `var1` is address width for each LUT
    - `var2` is number of cascaded MUX in each LUT
  - MATLAB_Script:
    - main Script for VHDL code-generation
  - Vivado:
    - synthesised Vivado project files, includes simulation
  - Bit_file:
    - Bitstream file uploaded to FPGA for verification
  - Reference:
    - some reference on distributed arithmetic and VHDL programming

## Instructions for use  
1.open `VHDL_Coder.mlx` in `\MATLAB_Script`  
2.Set the FIR parameters such as Taps, sampling frequency, cut-off frequency, window function, filter type
