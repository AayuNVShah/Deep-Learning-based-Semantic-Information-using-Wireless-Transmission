# DeepSC-ST: Deep Learning-Based Semantic Information Transmission Through Imperfect CSI

## 📌 Overview

**DeepSC-ST** is a **deep learning-enabled semantic communication system** designed for efficient **speech transmission over wireless channels** with **imperfect Channel State Information (CSI)**.
Unlike traditional communication systems that focus on transmitting raw data, DeepSC-ST prioritizes **meaning** by extracting and transmitting **semantic features**—significantly reducing bandwidth requirements while maintaining high accuracy in **speech recognition** and **speech synthesis**.

## 🚀 Motivation

With the rapid rise of **6G** and **intelligent devices**, traditional communication systems face challenges in spectrum limitations and network congestion.
DeepSC-ST addresses this by:

* Compressing speech into **low-dimensional semantic features**
* Transmitting these over imperfect CSI conditions
* Reconstructing speech or text efficiently at the receiver
* Reducing network traffic while supporting intelligent speech tasks

## 🎯 Key Contributions

* **Novel Semantic Communication Model** for speech input with imperfect CSI at the transmitter.
* **Joint Semantic-Channel Coding Scheme** to handle noisy, fading, and dynamic channels.
* **Integrated Speech-to-Text & Speech Synthesis** with CNN + GRU-based semantic encoder.
* **Interactive Proof-of-Concept Demonstration** with real human speech input.
* **Superior Performance** over conventional methods, especially in low-SNR environments.

## 🏗 System Architecture

The model consists of:

1. **Preprocessing** – Converts speech into spectrograms using Hanning window, FFT, and normalization.
2. **Semantic Encoder** – CNN + Bidirectional GRU to extract semantic features.
3. **Channel Encoder** – Transforms semantic features for transmission over wireless channels.
4. **Receiver Side** – Decodes features, reconstructs text, and optionally synthesizes speech.
5. **Greedy Decoder** – Uses CTC Loss for optimal text transcription.

## 📂 Dataset

* **LJ Speech Dataset** – 13,100 short audio clips (\~24 hours) with transcripts.
* 90% training / 10% validation split.
* Single-speaker, clean audio for robust model training.

## ⚙️ Training & Testing

### Training

* CNN + GRU-based semantic encoder
* CTC Loss optimization
* SGD with tuned learning rates (best results at 0.0001)

### Testing

* Evaluated under **Perfect CSI** and **Imperfect CSI**
* AWGN channel simulations
* SNR variation analysis for real-world applicability

## 📊 Results

* **Faster Convergence** under perfect CSI, but robust performance under imperfect CSI.
* **WER (Word Error Rate)** significantly lower than baseline systems.
* **Low-SNR Advantage** – Maintains better recognition accuracy where traditional methods fail.

| Scenario      | Convergence Speed | WER at Low SNR |
| ------------- | ----------------- | -------------- |
| Perfect CSI   | Fast              | Very Low       |
| Imperfect CSI | Moderate          | Low            |

## 🛠 Initialization

```bash
# Clone the repository
git clone https://github.com/AayuNVShah/Deep-Learning-based-Semantic-Information-using-Wireless-Transmission.git
cd Deep-Learning-based-Semantic-Information-using-Wireless-Transmission/DeepSC-ST_demonstration-Imperfect_CSI
```

## 📌 Future Scope

* Extend DeepSC-ST to support **image** and **video** semantic transmission.
* Improve channel estimation for **more robust imperfect CSI handling**.
* Deploy real-time **multi-user semantic communication systems**.

## 👥 Authors

* Aagam Shah, Aastha Gaudani, Aayushi Shah, Dhairya Shah
* Supervised by **Dr. Dhaval K. Patel**
* Teaching Assistant: **Kashish Shah**
