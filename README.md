# CIFAR-10 Deep Learning 

Exploration of CNN architectures on CIFAR-10 using PyTorch. Implements and compares modified AlexNet, VGG-11, ResNet-11, and ResNet-18 from scratch, with dropout regularisation experiments across all four families.

## Repository Structure

```
CNNs
    ├── AlexNet.ipynb       # Modified AlexNet + dropout experiments
    ├── VGG11.ipynb         # Adapted VGG-11 + dropout experiments  
    ├── ResNet.ipynb        # ResNet-11 and ResNet-18 + dropout experiments
    ├── env.yml             # Conda environment with all dependencies
    └── README.md
```

## Setup
```bash
conda env create -f env.yml
conda activate dl
```

## Results Summary

| Architecture | Params | Test Accuracy |
|---|---|---|
| AlexNet (p=0.3) | 848K | 74.01% |
| VGG-11 (p=0.3) | 13.55M | 69.01% |
| ResNet-11 (p=0.3) | 4.90M | 82.15% |
| ResNet-18 (p=0.3) | ~11.17M | 84% |

All models trained on CIFAR-10 (45k train / 5k val / 10k test), random seed 42, SGD with momentum 0.9, weight decay 1e-4, batch size 128, cosine annealing learning rate scheduler where applicable.

## Hardware

Trained on Google Colab T4 GPU and Apple M-series MPS.
