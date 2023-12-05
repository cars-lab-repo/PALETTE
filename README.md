# PALLETE: Risk-Aware and Explainable Framework for Ensuring Guaranteed Coverage in Evolving Hardware Trojan Detection
This repository contains various components related to the research paper and source codes of the evolving hardware Trojan detection framework.  </br>
[Rahul Vishwakarma](https://github.com/rahvis) & [Amin Rezaei](https://github.com/r3zaei) </br>

## Dataset 
We have used two different dataset for the detection of hardware Trojans. 

**Note**: The relevant dataset needs to be accessed from the below dataset source. <br>
**We are not providing dataset in our GitHub repo for Trust-Hub Chip Level Trojan benchmark.**  

### 1. Synthetic dataset: CASlab GAINESIS Tool
The dataste has binary label: _Trojan Free and Trojan Infected_. The benchmark distribution consists of a total 18 types of circuits. Specifically, our benchmark consists of 14 synchronous and 4 asynchronous circuits. Sychronous circuits are, AES, B15, ETHERNETMAC10GE, MEMCTRL, PIC16F84, RS232, S1423, S13207, S15850, S35932, S38417, S38584, VGALCD and WB_CONMAX. Asychronous circuits are, C2670, C3540, C5315 and C6288.

Source: https://caslab.e-ce.uth.gr/ToolsandDatabases.html

### 2. Trust-Hub:  Chip Level Trojans 
The dataste has binary label: _Trojan Free and Trojan Infected_. We include a third label: _Evolved Hardware Trojans_ using conformalized GAN. 

Source: https://trust-hub.org/#/benchmarks/chip-level-trojan

## Solution 
![Solution](https://github.com/cars-lab-repo/PALETTE/assets/64368687/db8b0d56-426e-45d9-bed7-0b84d175433a)

## Experiments
Use the below notebooks for reproducing the results in the paper. 

### 1. Generate 10,000 data points using conformalized GAN. 
This uses the existing input dataste and apply cGAN. 
```
01_conformalized_GAN/conformalized_GAN_8000epoch_10000data_points.ipynb
```

### 2. Results for GAINESIS dataset.
Provides the confidence and credibility plots.
```
02_synthetic_guaranteed_coverage_p_vales.ipynb
```

### 3. Results for TrustHub Chip-Level Trojan dataset.
This has three notebooks. The first one detects the evolving hardware Trojans. 
```
01_detect_evolving_trojans.ipynb
```
The below notebook calculates the p-values and based on the significance level, it provides the confidence score with guaranteed coverage. 
```
02_guaranteed_coverage_p_vales.ipynb
```
Finally, we also compare the performance with state of the art classifier. 
```
03_Logistic Regression.ipynb
```

### 4. Calibrated Explainability 
The notebook provides the explainability while rejecting a prediction. 
```
calibrated_explainability_for_rejecting_prediciton.ipynb
```
Sample explaination output are placed in the below directory. 
```
03_calibrated_explainability/calibrated_explainability/
explanation_0.html
explanation_1.html
explanation_2.html
explanation_3.html
```

## Features
- Generates evolved hardware Trojans from a given dataset.
- Provides guaranteed coverage of detected hardware Trojans.
- Calibrated explanations for the rejected decisions. 
- A novel method for risk-aware ranking of Trojans.

## License
GNU General Public License v3.0

## Citation
```
@INPROCEEDINGS{PALLETE,
  author={Vishwakarma, Rahul and Rezaei, Amin},
  booktitle={2023 IEEE/ACM International Conference on Computer Aided Design (ICCAD)}, 
  title={Risk-Aware and Explainable Framework for Ensuring Guaranteed Coverage in Evolving Hardware Trojan Detection}, 
  year={2023},
  volume={},
  number={},
  pages={1-9},
  doi={10.1109/ICCAD57390.2023.10323655}
}
