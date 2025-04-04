# Audio-Deepfake-Detection-
A lightweight and efficient solution for detecting AI-generated synthetic speech using ResNet-18 trained on log-mel spectrograms. Designed for simplicity, speed, and ease of deployment.
# Audio Deepfake Detection with ResNet-18

A lightweight and efficient solution for detecting AI-generated synthetic speech using **ResNet-18** trained on log-mel spectrograms. Designed for simplicity, speed, and ease of deployment.

---

## 🔍 Overview  
This repository implements a ResNet-18-based model to classify audio clips as **real** or **fake**. The model processes log-mel spectrograms of audio signals to detect artifacts introduced by AI-based voice synthesis (e.g., TTS, voice conversion).  

![ResNet-18 Architecture](https://miro.medium.com/v2/resize:fit:720/format:webp/1*Dk4Y5hXQO5ODUQh7j8gqJg.png)  
*Simplified ResNet-18 architecture with skip connections.*

---

## 🚀 Key Features  
- **Lightweight Model**: ResNet-18 (11.7M parameters) ensures fast inference (~50 ms/clip on CPU).  
- **Log-Mel Spectrograms**: Extracts time-frequency features for robust artifact detection.  
- **Pre-trained Weights**: Leverages ImageNet initialization for faster convergence.  
- **Real-Time Ready**: Optimized for deployment on edge devices.  

---

## 📂 Datasets  
1. **ASVspoof 2021 DF**  
   - Download: [ASVspoof 2021](https://www.asvspoof.org/)  
   - Contains 533,928 audio clips (real and synthetic).  
2. **In-the-Wild Dataset**  
   - Download: [In-the-Wild Dataset](https://github.com/yzyouzhang/AIR-ASVspoof)  
   - Real-world audio clips with background noise and compression artifacts.  

---
## Critical Files
ResNet-18 Model: https://gist.github.com/Hari0002/605834f6cb2978afa7bb3e7735be10b2

Training Script: https://gist.github.com/Hari0002/96c419e0deff6e90ee087e9d431edde7

Inference Script: https://gist.github.com/Hari0002/cea9a0e33b482bfdac9e1f6d7c349d79

jupyter Notebook implementation: https://gist.github.com/Hari0002/217176bab5a288e1aa51774d673b2bc0

## ⚙️ Setup  
1. Install dependencies:  
   ```bash  
   pip install -r requirements.txt  # Requires PyTorch, Librosa, Torchaudio  
---
## 📊 Performance
Dataset	     , EER (%)	 ,  Accuracy (%):
1) ASVspoof2021DF,	  8.21	,    92.5
2) In-the-Wild	,     12.37	,,    85.3
## 🌟 Future Improvements
Hybrid features (spectrograms + raw waveform embeddings).

Dynamic data augmentation (e.g., codec simulation).

Quantization for edge deployment (TensorRT/TFLite).
