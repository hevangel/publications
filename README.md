# My Publications

## How to test the whole firmware/software when the RTL can’t fit the emulator - DVCON2019 (best paper award 2nd place)

Pre-silicon firmware and software (FW/SW) testing is a necessity for all silicon companies. One of the biggest challenge is when the RTL cannot fit inside the emulator. In verification, it is a common practice to black box unused logic in the RTL to reduce gate count. However, adopting this approach in emulation has unique challenges due to the difference in the architecture of an UVM testbench compared to the actual FW/SW. In this paper, we will present our strategy on how to run the full FW/SW on blackboxed RTL in the emulator using a Hybrid Software Simulator (HSWSIM). The paper will compare the benefit of our strategy over using existing solutions, such as virtual platform. Then the paper will describe the architecture of the HSWSIM and outline its two use models, one to test user space FW code and the other to test kernel space FW code. The final section of the paper presents the results of using HSWSIM to bring up the FW/SW in our latest generation chip.

## Pre-Silicon SW/FW Testing with Protium S1 A Case Study - CDNLIVE2018 (best paper award SoC/System Verification Track)

A case study of pre-silicon SW/FW testing using Protium S1.  Boot up Linux in the embedded ARM core successfully.  Verify the PCIe interface is working as expected and test out low level FW download procedures.  Verify the ARM CoreSight is wired up correct with live interaction of the DSTREAM probe.  All major datapath are up and running in the first SW release.  

## Speedup the Debug Turnaround Time and Regression Run Time with SystemVerilog/UVM Test Dynamic Load - CDNLIVE2018 

Present a verification methodology using the new SystemVerilog dynamic load feature in the Xcelium simulator, which mimics the old dynamc load feature in Specman.  RTL debug turnaround time is speeded up by 90% and the total regression time is reduced by 25%.

## IDEs SHOULD BE AVAILABLE TO HARDWARE ENGINEERS TOO! - DVCON2018

Modern integrated development environments (IDEs) represent a new era of tools for code development and debug, and are pushing out legacy software development environments in Vim and Emacs. However, why limit using these tools exclusively in the software world? When in fact the benefits of using a GUI based development environment for HDL programming has a direct impact on the hardware development and verification effort required. This paper illustrates the advantages of using SystemVerilog IDEs which, when properly employed, can help decrease debug and turnaround times related to code compilation and simulation, improve code readability, comprehension and maintainability, and boost productivity.

## UVM Interactive Debug Library: Shortening the Debug Turnaround Time - DVCON2017

Interactive debug in System Verilog simulations is not a natively supported feature, unlike other Hardware Verification Languages (HVL) such as Specman e. In this paper we are presenting an interactive debug library for UVM[1] implemented in the SystemVerilog Direct Programming Interface (SV-DPI)[2]. At a basic level, this enables high level interactive debug at simulation run time. The features of this library includes: 1) writing or reading a register via the UVM register abstraction layer, 2) creating, randomizing, initializing, and starting a UVM sequence on any sequencer, and 3) calling a user defined SV function or task from the interactive debug prompt. We are also presenting a debug and regression methodology outlining the best practice on how to speed up debug and minimize the regression run time. The preliminary results show that using interactive debug library significantly reduced the debug turnaround time and regression run time. Users can retest different scenario in matter of seconds instead of waiting minutes or hours for the testbench to recompile, elaborate, and rerun the simulation from time zero. The uvm_debug library is available as an open-source project in github
