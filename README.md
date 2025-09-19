# HADQ-Net: A Power-Efficient and Hardware-Adaptive Deep Convolutional Neural Network Translator Based on Quantization-Aware Training for Hardware Accelerators

[![Paper](https://img.shields.io/badge/Paper-Electronics-3686-blue)](https://doi.org/10.3390/electronics14183686)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)

[![DOI](https://img.shields.io/badge/DOI-10.3390/electronics14183686-blue)](https://doi.org/10.3390/electronics14183686)  
[![Journal](https://img.shields.io/badge/Journal-Electronics-green)](https://www.mdpi.com/journal/electronics)  
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)  
Official PyTorch implementation of the paper:  
**"HADQ-Net: A Power-Efficient and Hardware-Adaptive Deep Convolutional Neural Network Translator Based on Quantization-Aware Training for Hardware Accelerators"**  
Published in *Electronics* 2025, 14(18), 3686.

> **Cite our work:**  
> Oflamaz, C.U.; Yalçın, M.E. HADQ-Net: A Power-Efficient and Hardware-Adaptive Deep Convolutional Neural Network Translator Based on Quantization-Aware Training for Hardware Accelerators. *Electronics* **2025**, *14*, 3686. https://doi.org/10.3390/electronics14183686

## ✨ Overview

HADQ-Net is a novel **Quantization-Aware Training (QAT)** framework designed to optimize Deep Convolutional Neural Networks (CNNs) for deployment on resource-constrained **edge devices** and hardware accelerators (FPGAs, GPUs, TPUs, DPUs).

By compressing 32-bit floating-point (FP32) models to lower bit-widths (down to 1-bit), HADQ-Net significantly reduces **memory footprint**, **computational complexity**, and **energy consumption** while maintaining competitive accuracy. Our method features **adaptive quantization limits** and **normalization techniques** based on layer/channel statistics for enhanced performance.


## 🚀 Key Features

*   **Hardware-Adaptive Quantization:** Achieves SOTA accuracy across a wide range of bit-widths (1-bit to 8-bit).
*   **Superior Performance:** Outperforms established methods like **DoReFa-Net** and **PACT**, especially at 4-bit and above.
*   **Comprehensive Support:** Algorithms for QAT, quantized convolution, and efficient integer-only inference.
*   **Extensive Validation:** Tested on **Classification** (ResNet, DenseNet, EfficientNet), **Object Detection** (YOLOv7, Faster R-CNN), **Semantic Segmentation** (Mask R-CNN), and **Super-Resolution** (VDSR, SRCNN, etc.).
*   **Hardware-Friendly:** Designed for seamless deployment on edge devices, significantly reducing latency and power consumption.
*   Adaptive, per-layer / per-channel clipping and normalization  
*   Supports **fixed- and mixed-precision** quantization (1–8 bits)  


## 📊 Benchmark Results (Summary)

### vs. State-of-the-Art on CIFAR-100 (ResNet18)
| Method          | 3/3 bits | 4/4 bits     | 5/5 bits     | 8/8 bits     |
|-----------------|----------|--------------|--------------|--------------|
| DoReFa-Net      | 77.7%    | 79.7%        | 81.0%        | 82.2%        |
| PACT            | 79.0%    | 81.6%        | 82.3%        | 84.6%        |
| **HADQ-Net**    | **79.7%**| **86.2%**    | **90.1%**    | **91.0%**    |

### QAT vs. Post-Training Quantization (PTQ)
| Quantization Type | 4/4 bits     | 8/8 bits     |
|-------------------|--------------|--------------|
| PTQ               | 67.9%        | 87.5%        |
| **QAT (HADQ-Net)**| **86.2%**    | **91.0%**    |

### Model Size Reduction
| Precision | Model Size (MB) | Compression Ratio |
|-----------|-----------------|-------------------|
| FP32      | 41.94           | 1x                |
| 8-bit     | 10.49           | 4x                |
| 4-bit     | 5.24            | 8x                |
| 2-bit     | 2.62            | 16x               |

*For full results on detection mAP, segmentation AP, and super-resolution PSNR, please see the [paper](https://doi.org/10.3390/electronics14183686).*

## 📧 Contact
**Can Uğur Oflamaz    :** cuoflamaz@run-x.com

**Müştak Erhan Yalçın :** mustak.yalcin@itu.edu.tr

**Github Link         :** https://github.com/can-ugur/HADQ-Net

## 🙏 Acknowledgements
This research was funded by **Aselsan Inc.**. We thank the **Istanbul Technical University Electronics and Communication Engineering Department** for their support.
