# Risk-Aware and Explainable Framework for Ensuring Guaranteed Coverage in Evolving Hardware Trojan Detection (_ICCAD 2023_)
### The source code for the paper has been made availabe only for the Reviewers of ICCAD and the code has not been published online. 
[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

## Dataset 
We have used two different dataset for the detection of hardware trojans. 

### 1. Synthetic dataset: CASlab GAINESIS Tool
The dataste has binary label: _Trojan Free and Trojan Infected_. The benchmark distribution consists of a total 18 types of circuits. Specifically, our benchmark consists of 14 synchronous and 4 asynchronous circuits. Sychronous circuits are, AES, B15, ETHERNETMAC10GE, MEMCTRL, PIC16F84, RS232, S1423, S13207, S15850, S35932, S38417, S38584, VGALCD and WB_CONMAX. Asychronous circuits are, C2670, C3540, C5315 and C6288.

Source: https://caslab.e-ce.uth.gr/ToolsandDatabases.html

### 2. Trust-Hub:  Chip Level Trojans 
The dataste has binary label: _Trojan Free and Trojan Infected_. We include a third label: _Evolved Hardware Trojans_ using conformalized GAN. 

Source: https://trust-hub.org/#/benchmarks/chip-level-trojan



## Features
- Generates evolved hardware trojans from a given set of dataset.
- Provides guaranteed coverage of detected hardware trojans.
- Calibrated explanations for the rejected decisions. 
- A novel method for risk-aware ranking of trojans.

## License
MIT
