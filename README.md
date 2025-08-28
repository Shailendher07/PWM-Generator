# Verilog PWM Generator

## Project Overview
This project implements a Pulse Width Modulation (PWM) Generator using behavioral RTL coding in Verilog, along with a testbench for functional verification.  
The design allows configurable PWM duty cycle based on an input threshold value.

PWM is widely used in:
- Motor speed control  
- LED brightness control  
- Signal modulation  
- Digital-to-analog conversion (DAC) using filtering  

## Features
- 8-bit PWM resolution  
- Configurable duty cycle via `threshold` input  
- Synchronous reset for reliable startup  
- Load control to update duty cycle dynamically  
- Testbench included for simulation and verification  

## Design Description
### RTL Module: `pwm.v`
- Inputs:
  - `clk` : System clock  
  - `reset` : Active-high reset  
  - `load` : Updates PWM compare register with new threshold  
  - `threshold [7:0]` : Duty cycle control (0–255 → 0%–100%)  

- Outputs:
  - `pwm_out` : Generated PWM waveform  
  - `pwm_reg [7:0]` : Current counter value (for debug/observation) 
