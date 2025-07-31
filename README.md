# GAN_assignment

# QuickDraw Creative AI Project

## Overview

This repository contains the implementation and analysis of:  
- Creative AI – training DCGANs on QuickDraw sketch categories of increasing complexity: **smiley faces**, **swords**, and **cats**. Includes comparative analysis, learning-rate tuning, and extensions.

## Title

**Generative Adversarial Modeling of QuickDraw Sketches: A Comparative Study from Smiley Faces to Cats**

---

## Repository Structure
---
├── README.md # This file
├── Quickdraw_dcgan.ipynb # Notebook: DCGAN on smiley, sword, cat sketches
├── model_flowchart.png # Flowchart of the DCGAN architecture
├── gan_pipeline_flowchart.png # Pipeline flowchart (data → model → analysis)
├── smiley.npy # QuickDraw smiley face data (downloaded)
├── sword.npy # QuickDraw sword data (downloaded)
├── cat.npy # QuickDraw cat data (downloaded)
├── outputs/ # Generated samples, loss plots, etc.
│ ├── smiley/
│ ├── sword/
│ └── cat/
└── report/ # (optional) markdown or PDF version of the write-up

---
---

## Key Features

- Implementation of basic GAN and deep variants for synthetic data (sine wave, noisy parametric curve).  
- DCGAN implementation in PyTorch for image sketch generation.  
- Training on three QuickDraw categories: smiley faces (low complexity), swords (moderate), cats (high).  
- Learning-rate balancing to stabilize adversarial training.  
- Visual comparison of real vs. generated sketches.  
- Flowcharts for methodology and model architecture.  
- Analytical write-up on performance vs. sketch complexity, observations, and recommendations.

---

## Dependencies

Tested with Python 3.9+. Main dependencies:

- torch  
- torchvision  
- numpy  
- matplotlib  
- graphviz  
- medmnist (if revisiting medical option)  
- jupyter (for notebooks)
---
## Install with:

```bash
pip install torch torchvision numpy matplotlib graphviz
---
---
## Data Download

wget -O smiley.npy "https://storage.googleapis.com/quickdraw_dataset/full/numpy_bitmap/smiley%20face.npy"
wget -O sword.npy "https://storage.googleapis.com/quickdraw_dataset/full/numpy_bitmap/sword.npy"
wget -O cat.npy "https://storage.googleapis.com/quickdraw_dataset/full/numpy_bitmap/cat.npy"
---
---
''' bash
jupyter notebook part2_quickdraw_dcgan.ipynb
---
---
1. Loads and preprocesses QuickDraw data (padding, normalization).

2. Defines DCGAN generator and discriminator.

3. Trains GANs on smiley, sword, and cat categories with learning-rate tuning.

4. Visualizes training loss curves and real vs. generated sketches.

5. Includes extension to compare classes and complexity.
---
