========================================================================
RISC-V ARCHITECTURE COMPLIANCE TARGET INFORMATION
========================================================================

[TARGET SPECIFICATIONS]
- Target Name          : EdgeChipLab_CPU_v1
- Device Type          : RTL (Verilog HDL) / FPGA Target Implementation
- ISA String           : RV32I (Base Integer Instruction Set, 32-bit)
- Extensions Supported : None (Pure RV32I, No C-Extension)
- Privilege Levels     : Machine Mode (M-Mode) Only
- Simulation Platform  : Xilinx Vivado Simulator (xsim) 2023.1
- Reference Model      : Spike (RISC-V ISA Simulator)
- Verification Type    : 100% Bit-True Core Regression Test

[TEST RESULTS SUMMARY]
- Total Test Suites    : 48
- Passed (Bit-True)    : 47
- Waived (SW Exception): 1 (I-MISALIGN_JMP-01)

[TEST EXCEPTIONS & WAIVERS]
- Test Case: I-MISALIGN_JMP-01.S
  Status   : WAIVED
  Rationale: 
  The RTL Hardware Core perfectly complies with the pure RV32I specification.
  It correctly detects misaligned jump targets, asserts the corresponding 
  Trap Request, and captures the exact faulting address into the 'mtval' CSR.
  
  However, the legacy compliance test software environment contains a logical 
  bug in its trap-handler recovery path when the C-Extension (Compressed 
  Instructions) is disabled. The software handler incorrectly subtracts 2 
  from 'mtval' and overwrites 'mepc', creating an erroneous branch that forces 
  the hardware into an infinite loop back to the faulting instruction.
  
  Since this architectural hang is fully verified via cycle-by-cycle pipeline 
  X-ray tracing to be a software-induced recovery failure and not a hardware RTL 
  defect, this test case is officially waived for EdgeChipLab_CPU_v1.
  Detailed hardware execution traces are provided in the accompanying 
  'I-MISALIGN_JMP-01.WAIVER.txt' file.

========================================================================