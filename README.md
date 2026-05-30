# EdgeChipLab_CPU_v1 Successfully Passed RISC-V RV32I ACT v3.0

Verified by cycle-by-cycle bit-true regression against Spike reference model.

## Official Public Compliance Report

**EdgeChipLab_CPU_v1** is a custom pure-Verilog educational RISC-V CPU core developed at **EdgeChipLab**.

This RTL core has successfully completed the **RISC-V RV32I Architectural Compatibility Tests (ACT v3.0)** using cycle-by-cycle bit-true verification against the Spike reference model.

---

## Compliance Summary

| Item            |                Result |
| --------------- | --------------------: |
| ISA             |                 RV32I |
| RTL Language    |           Verilog HDL |
| Privilege Mode  | Machine Mode (M-Mode) |
| Simulator       |    Vivado xsim 2023.1 |
| Reference Model |                 Spike |
| Total Tests     |                    48 |
| Passed          |                    47 |
| Waived          |                     1 |

### Result

✅ **EdgeChipLab_CPU_v1 successfully passed RV32I ACT v3.0**

---

## Public Acknowledgement

Official RISC-V Arch-Test Issue:

https://github.com/riscv/riscv-arch-test/issues/1600

The repository maintainer confirmed:

> “Congratulations on building a core that passes the RV32I ACTs v. 3.0!”

This public acknowledgement provides meaningful external validation of the hardware verification result.

---

## Educational Roadmap

This compliance milestone is part of the broader EdgeChipLab semiconductor system education roadmap:

**RTL Design → RISC-V CPU → Architectural Verification → NPU Integration → FPGA Edge AI System**

The verified CPU core is planned for integration with our custom RTL-based AI NPU into a complete memory-mapped FPGA SoC platform.

---

## Related Book

### AI NPU System Design with Python and Verilog

**Roger Kim (Hyo Seob Kim)**

Amazon:
https://www.amazon.com/dp/B0GLQVJWMK

The book explains:

* Custom RTL NPU design
* Python + Verilog bit-true verification
* FPGA implementation
* End-to-end hardware system construction

This knowledge directly supports the upcoming:

**Verified RISC-V CPU + Custom NPU + Memory-Mapped SoC + FPGA Integration**

---

## Repository Contents

* README.md
* EdgeChipLab_RV32I_Compliance_Submission.zip
* Signature outputs
* Target specification
* Waiver analysis
* Bit-true verification traces

---

## Maintained by

**EdgeChipLab**
https://www.semiconductorschool.co.kr
