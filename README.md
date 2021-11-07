# Abstracts:

## How to test the whole firmware/software when the RTL can’t fit the emulator - DVCON2019 (best paper award 2nd place)
[paper](dvcon2019%20SW%20Emulation%20paper.pdf) [slides](dvcon2019%20SW%20Emulation%20slides.pptx))

Pre-silicon firmware and software (FW/SW) testing is a necessity for all silicon companies. One of the biggest challenge is when the RTL cannot fit inside the emulator. In verification, it is a common practice to black box unused logic in the RTL to reduce gate count. However, adopting this approach in emulation has unique challenges due to the difference in the architecture of an UVM testbench compared to the actual FW/SW. In this paper, we will present our strategy on how to run the full FW/SW on blackboxed RTL in the emulator using a Hybrid Software Simulator (HSWSIM). The paper will compare the benefit of our strategy over using existing solutions, such as virtual platform. Then the paper will describe the architecture of the HSWSIM and outline its two use models, one to test user space FW code and the other to test kernel space FW code. The final section of the paper presents the results of using HSWSIM to bring up the FW/SW in our latest generation chip.

## Pre-Silicon SW/FW Testing with Protium S1 - CDNLIVE2018 (best paper award SoC/System Verification Track)
[slides](cdnlive2018%20Presilicon%20SW%20Testing%20with%20Protium%20S1%20slides.pptx)

A case study of pre-silicon SW/FW testing using Protium S1.  Boot up Linux in the embedded ARM core successfully.  Verify the PCIe interface is working as expected and test out low level FW download procedures.  Verify the ARM CoreSight is wired up correct with live interaction of the DSTREAM probe.  All major datapath are up and running in the first SW release.  

## Speedup the Debug Turnaround Time and Regression Run Time with SystemVerilog/UVM Test Dynamic Load - CDNLIVE2018 
[slides](cdnlive2018%20SystemVerilog%20Dynamic%20Load%20slides.pptx)

Present a verification methodology using the new SystemVerilog dynamic load feature in the Xcelium simulator, which mimics the old dynamc load feature in Specman.  RTL debug turnaround time is speeded up by 90% and the total regression time is reduced by 25%.

## IDEs SHOULD BE AVAILABLE TO HARDWARE ENGINEERS TOO! - DVCON2018
[paper](dvcon2018%20SystemVerilog%20IDE%20paper.pdf) [slides](dvcon2018%20SystemVerilog%20IDE%20slides.ppt)

Modern integrated development environments (IDEs) represent a new era of tools for code development and debug, and are pushing out legacy software development environments in Vim and Emacs. However, why limit using these tools exclusively in the software world? When in fact the benefits of using a GUI based development environment for HDL programming has a direct impact on the hardware development and verification effort required. This paper illustrates the advantages of using SystemVerilog IDEs which, when properly employed, can help decrease debug and turnaround times related to code compilation and simulation, improve code readability, comprehension and maintainability, and boost productivity.

## UVM Interactive Debug Library: Shortening the Debug Turnaround Time - DVCON2017
[paper](dvcon2017%20UVM%20Debug%20Library%20paper.pdf) [slides](dvcon2017%20UVM%20Debug%20Library%20slides.ppt)

Interactive debug in System Verilog simulations is not a natively supported feature, unlike other Hardware Verification Languages (HVL) such as Specman e. In this paper we are presenting an interactive debug library for UVM[1] implemented in the SystemVerilog Direct Programming Interface (SV-DPI)[2]. At a basic level, this enables high level interactive debug at simulation run time. The features of this library includes: 1) writing or reading a register via the UVM register abstraction layer, 2) creating, randomizing, initializing, and starting a UVM sequence on any sequencer, and 3) calling a user defined SV function or task from the interactive debug prompt. We are also presenting a debug and regression methodology outlining the best practice on how to speed up debug and minimize the regression run time. The preliminary results show that using interactive debug library significantly reduced the debug turnaround time and regression run time. Users can retest different scenario in matter of seconds instead of waiting minutes or hours for the testbench to recompile, elaborate, and rerun the simulation from time zero. The uvm_debug library is available as an open-source project in github

## SW/FW Automated Test Framework and Debug Toolkit for System Testing - DAC2016
[slides](dac2016%20FWSW%20Test%20Framework%20slides.pdf)

Lessons learnt from migrating the old C-only ah-doc direct testcases to C++11/14 automated test framework built on GoogleTest.  The new test framework uses new language features of C++11/14 increase productivity and reduce human errors.  The test framework  has a built-in tcl server control test equipment directly from C++ code.  It also supported fully automated regression with Jenkin and Jira integration.

## A Methodology to Port a Complex Multi-Language Design and Testbench for Simulation Acceleration - DVCON2015
[paper](dvcon2015%20Palladium%20Simulation%20Acceleration%20paper.pdf) [slides](dvcon2015%20Palladium%20Simulation%20Acceleration%20slides.pptx)

PMC's verification teams started exploring simulation acceleration (SA) with hardware-assisted verification in 2011, as one of the early adopters of UVM Acceleration. They undertook this effort because of the complexity and size of their mixed-language designs, which were coded in SystemVerilog, Verilog, and VHDL, and stimulated using state-of-the-art testbenches coded in UVM-e.

A few years later, the task of porting a design and testbench from simulation to acceleration evolved into a methodology and is now re-used across multiple verification teams. Finally, PMC has achieved the holy grail of SA, conquering the most complex challenges of SA verification including: 1) Speed – achieving 67x speed up, 2) Time to First Test – taking only a month to port a verification environment to run in acceleration mode, 3) Consistent – Running the same tests with RTL and an accelerated DUT, producing the same results.

This methodology exploits essential capabilities of the tools in use, and production proven procedures. This paper outlines a step-by-step guide to port an existing UVM-e testbench to SA. The verification user community can use this paper as a template to plan their migration from simulation to hardware acceleration.

## Can You Even Debug a 200M+ Gate Design? - DVCON2013
[paper](dvcon2013%20Debug%20Techniques%20paper.pdf) [slides](dvcon2013%20Debug%20Techniques%20slides.pptx)

Abstract—Verification debug consumes a large portion of the overall project schedule, and performing efficient debug is a key concern in ensuring projects tape out on time and with high quality. In this paper, we outline a number of key verification debug challenges we were faced with and how we addressed them using a combination of tools, technology and methodology. The root cause of failures can be traced, most often, to either an issue in the RTL, an issue in the testbench or, in our case, the software interacting with the hardware. Speeding the debug turnaround time (the time to re-run a failing sim to replicate the issue for debug) is critical for efficient debug. Periodic saving of the simulation state was utilized extensively to narrow the debug turnaround time to a very small window. Once a re-run was launched, waveform verbosity levels could be set by users to dump the appropriate amounts of information for debug of the re-run scenario. For additional performance on the testbench side, coding methodology was introduced that allowed for maximum performance of stable sections of code. To speed SW debug, a software driver was implemented into the testbench to allow for debug of SW related issues very early on in the project.

## Maximize Vertical Reuse, Building Module to System Verification Environments with UVM e - DVCON2013
[paper](dvcon2013%20Veritical%20Reuse%20paper.pdf) [slides](dvcon2013%20Veritical%20Reuse%20slides.pptx)

Given the size and complexity of modern ASICs/SoC, coupled with their tight project schedule, it is impractical to build a complete system or chip level verification environment from scratch. Instead, in order to increase productivity, maximizing reuse of existing verification components seamlessly with the project has become one of the biggest opportunities to increase verification efficiency. In this paper, we present a testbench framework to maximize vertical reuse within a project. The framework presented here has been proven on the ground-up development of a 200M gate ASIC. In our framework, the system testbench is built in a hierarchical manner by recursively importing lower level block or module testbenches. From the lowest level to the highest level, all the testbenches are designed to support plug-and-play integration. Verification engineers can hook up several lower level testbenches and turn them into a higher level testbench. The system testbench inherits the device configuration sequences, traffic generation sequences, checkers and monitors from the imported module testbenches without duplication of effort. As a result, vertical reuse shortens the development time of the system testbench, improves the quality of testbench code and allows fast bring up during system integration.

## Hardware/Software co-verification using Specman and SystemC with TLM ports - DVCON2012
[paper](dvcon2012%20HWSW%20Coverification%20paper.pdf) [slides](dvcon2012%20HWSW%20Coverification%20slides.ppt)

In modern ASIC/SoC design, the hardware and software have to work seamlessly together to deliver the functions, requirements and performance of the embedded system. To accelerate time-to-market and to reduce overall development cost, it is crucial to co-verify the software code with the hardware design prior to tape-out. The software team can start developing and debugging their code with the actual hardware RTL code to shorten their overall development cycle. The hardware team can use the software code to identify performance bottlenecks and incorrect functional behaviors early in the development cycle which helps to reduce the risk of increasingly expensive device revisions.

The current approach to co-verification is primarily running the software on the embedded processor inside the hardware design, either within the simulator or with ICE (in-circuit emulation). The disadvantage of this approach is slow debug turnaround time and the higher cost is procuring and supporting a dedicated emulation box or FPGA platform. In addition, the software is running in isolation relative to the testbench, hence it is often challenging and inconvenient to integrate the software with other verification IP in the testbench.

In this paper, we will present an alternate approach on how to integrate the software driver into the simulator using Specman and SystemC with TLM ports. The software is running in the same memory space as the testbench, both of which run through the simulator on the Linux host. The advantage of this approach is fast execution speed of the software and the interoperability of the software with other verification components in the testbench. The software code runs in zero simulation time and the testbench has full control of the software using TLM ports and direct memory access via pointers. In addition, the software code can invoke gdb or any other C debugger to make debugging easier.


