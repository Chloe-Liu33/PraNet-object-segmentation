# EG-PraNet: Camouflaged Locust Segmentation

[![Paper](https://img.shields.io/badge/Paper-Computers_&_Electronics_in_Agriculture-blue.svg)](https://www.sciencedirect.com/science/article/abs/pii/S0168169922003787)
[![Dataset](https://img.shields.io/badge/Dataset-Locust--mini-green.svg)](https://github.com/Chloe-Liu33/Locust-mini)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> [cite_start]Official implementation of the paper: **"Camouflaged locust segmentation based on PraNet"** (Computers and Electronics in Agriculture, 2022)[cite: 757, 761].

## 📌 Overview

[cite_start]Precise detection and segmentation of camouflaged pests are critical for assisting plant protection robots in catching and killing locusts without large-scale pesticide spraying[cite: 772, 788]. [cite_start]This repository provides an end-to-end deep learning framework, **EG-PraNet**, designed to accurately segment locusts that camouflage themselves within complex agricultural backgrounds[cite: 773, 779]. 

[cite_start]By optimizing the feature extraction pipeline and enhancing data robustness, EG-PraNet achieves state-of-the-art efficiency and accuracy on the custom **Locust-mini** dataset[cite: 775, 779].

### ✨ Key Architectural Enhancements
* **Group Reverse (GR) Module:** We improved the original Reverse Attention (RA) module by grouping and fusing features. [cite_start]This reduces redundant convolution layers and multiplication calculations, lowering the calculating cost while extracting more useful information[cite: 776, 777].
* [cite_start]**Robust Image Augmentation:** To make the model more robust against complex field conditions, the training pipeline incorporates random pepper noise, color enhancement, random cropping, and resolution lowering[cite: 778].
* [cite_start]**Superior Performance:** Compared to the baseline PraNet, EG-PraNet increases the Dice coefficient by 0.126 and IoU by 0.152[cite: 780]. [cite_start]Furthermore, inference throughput is highly optimized for real-time robotic applications, achieving 16.4 fps on a Tesla K80[cite: 781, 1042].

## 🧠 Model Architecture

<p align="center">
  <img src="./assets/architecture.png" alt="Overview of EG-PraNet" width="90%">
</p>
<p align="center">
  <em>Fig. [cite_start]1: Overview of EG-PraNet, based on ResNet50 with one Parallel Partial Decoder (PPD) module and three Group Reverse (GR) modules[cite: 863, 953].</em>
</p>

## 🚀 Getting Started

### 1. Prerequisites
Clone the repository and install the required dependencies:
```bash
git clone [https://github.com/Chloe-Liu33/PraNet-object-segmentation.git](https://github.com/Chloe-Liu33/PraNet-object-segmentation.git)
cd PraNet-object-segmentation
pip install -r requirements.txt
