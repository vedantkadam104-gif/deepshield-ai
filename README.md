# 🛡️ DeepShield AI
### Multi-Domain Deepfake Detection System

![Python](https://img.shields.io/badge/Python-3.10-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-2.0-red)
![Accuracy](https://img.shields.io/badge/Accuracy-99.63%25-green)

## 🎯 Live Demo
👉 [Try DeepShield AI](https://73faf5ff3124411cb6.gradio.live)

## 📌 About
DeepShield AI is a state-of-the-art deepfake detection system that combines three parallel detection branches to identify fake faces with 99.63% accuracy.

## 🏗️ Architecture

Input Image (224×224) goes through 3 parallel branches:

- **CNN Branch (EfficientNet-B3)** → 1536 features — detects texture & blending artifacts
- **ViT Branch (ViT-B/16)** → 768 features — checks global facial consistency
- **Frequency Branch (DCT + FFT)** → 256 features — finds hidden GAN fingerprints

All 3 branches combined → Multi-Fusion Layer (2560 features) → **REAL ✅ / FAKE 🚨**

## 📊 Results

| Epoch | Train Acc | Val Acc |
|-------|-----------|---------|
| 1 | 90.44% | 98.65% |
| 2 | 97.54% | 98.92% |
| 3 | 98.42% | 98.90% |
| 4 | 99.12% | 99.52% |
| **5** | **99.38%** | **99.63% ⭐** |

## 🛠️ Tech Stack

| Component | Technology |
|---|---|
| Framework | PyTorch |
| CNN Backbone | EfficientNet-B3 (timm) |
| ViT Backbone | ViT-B/16 (timm) |
| Frequency | DCT + FFT (NumPy, SciPy) |
| Augmentation | Albumentations |
| Demo UI | Gradio |
| Training Platform | Kaggle (Tesla T4 GPU) |
| Dataset | 140k Real and Fake Faces |

## 📁 Dataset
- 70,000 Real faces (Flickr)
- 70,000 Fake faces (StyleGAN2)
- Split: 50k train / 10k val / 10k test

## 📈 Model Info
- Total Parameters: 100,097,162
- Model Size: 382.5 MB
- Best Val Accuracy: 99.63%

## 👨‍💻 Author
**Vedant Kadam**
M.Sc. Data Science & AI — SPPU, Pune
