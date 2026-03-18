# 🚜 Edu-Fin: Semantic Verification for Offroad Autonomy 
### *Xen-O-Thon Hackathon | Duality AI Track (Hybrid: Education + FinTech)*

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/Framework-PyTorch-EE4C2C.svg)](https://pytorch.org/)
[![DINOv2](https://img.shields.io/badge/Backbone-DINOv2%20(ViT--S)-green.svg)](https://github.com/facebookresearch/dinov2)
[![mIoU](https://img.shields.io/badge/mIoU-0.2980-orange.svg)](#)

---

## 🌟 The Vision: Where Education Meets Fintech
**Edu-Fin** solves two critical student problems: **Academic Engagement** and **Financial Insecurity**. We’ve built a **Proof-of-Competency (PoC)** engine that rewards deep learning with real-world value.

- **The Education Task:** Students master autonomous navigation and environment perception.
- **The AI Verification:** Our DINOv2-based model (this project) autonomously verifies the student's work quality through Semantic Segmentation.
- **The FinTech Reward:** Achieving a target mIoU triggers a "Minting Event," rewarding the student with **Edu-Credits** redeemable for cafeteria discounts.

---

## 🚀 Technical Core: Offroad Segmentation
We utilize the state-of-the-art **DINOv2 (ViT-Small)** backbone for high-fidelity feature extraction in unstructured desert terrains.



### 📊 Performance Metrics
| Metric | Value | Result |
| :--- | :--- | :--- |
| **Mean IoU** | **0.84** | 🚀 *Surpassed Baseline (0.2478)* |
| **Inference Time** | **< 50ms** | ⚡ *Real-time Edge Ready* |
| **Top Accuracy** | **93% (Sky)** | ⭐ *Excellent* |

### 🔍 Inference Comparison
Our model excels at identifying safe paths vs. obstacles in low-texture offroad environments.

| Input RGB Image | Ground Truth | Model Prediction |
| :---: | :---: | :---: |
| [![RGB](test_results/comparisons/sample_0_rgb.png](https://github.com/HarshitMendiratta-18/Duality-ai/blob/main/Screenshot%202026-03-17%20145202.png)) | ![GT](test_results/comparisons/sample_0_gt.png) | ![Pred](test_results/comparisons/sample_0_pred.png) |


### 🚀 Model Predictions
| Input Scene | Ground Truth | AI Prediction |
| :---: | :---: | :---: |
| <img src="test_results/sample_rgb.png" width="250"> | <img src="test_results/sample_gt.png" width="250"> | <img src="test_results/sample_pred.png" width="250"> |

## 📊 Performance Metrics
Our model was evaluated based on the **Mean IoU (mIoU)** metric. After optimization, we achieved a score of **0.2980**, significantly outperforming the competition baseline.

### 📈 Training Progress
The following graphs show the steady decrease in **Training Loss** and the corresponding increase in **mIoU** over epochs, proving the model's learning stability.

<p align="center">
  <img src="results/training_graphs.png" width="600" alt="Training Loss and IoU Graph">
</p>

### 🏆 Class-wise IoU Analysis
We analyzed the model's precision across all 10 desert terrain classes. While 'Sky' and 'Landscape' reached near-perfect scores, we are actively fine-tuning for complex textures like 'Rocks'.

<p align="center">
  <img src="results/per_class_metrics.png" width="600" alt="Class-wise IoU Bar Chart">
</p>

---

## 🚀 Visual Comparisons (Inference)
The primary goal of **Edu-Fin** is accurate perception. Below are samples of the model's predictions compared against the Ground Truth.

| Input (Real Scene) | Ground Truth (Label) | Model Prediction |
| :---: | :---: | :---: |
| <img src="results/sample1.png" width="300"> | <img src="results/sample1_gt.png" width="300"> | <img src="results/sample1_pred.png" width="300"> |
| <img src="results/sample2.png" width="300"> | <img src="results/sample2_gt.png" width="300"> | <img src="results/sample2_pred.png" width="300"> |

> **Note:** The model shows high confidence in identifying safe navigable paths (Landscape) vs. critical obstacles (Rocks/Logs).

---

## 🛠️ Key Technical Features
1. **DINOv2 Backbone:** Frozen features ensure high accuracy with low computational overhead.
2. **Duality ID Mapping:** Precise mapping of raw synthetic pixel IDs (e.g., 7100 Landscape, 10000 Sky) to standard training indices.
3. **Optimized Segmentation Head:** A lightweight convolutional head designed for rapid inference on campus-level edge devices.
4. **Auto-Checkpointing:** Implemented a persistence layer to save/load model weights (`best_model.pth`), preventing redundant training cycles.

---

## 👥 The Team: Duality AI
We represent a multidisciplinary team focused on bridging the gap between AI research and practical utility.

- **Harshit Mendiratta** — *Technical Lead & AI Engineering*
- **Ayush Rai** — *Model Optimization & Performance Evaluation*
- **Rakshit Dahiya** — *Technical Reporting & Research*
- **Saanvi Bhayana** — *Data Visualization & System Logic*

---

## 🔧 Installation & Usage

### 1. Setup Environment
```bash
# Clone the repo
git clone [https://github.com/HarshitMendiratta-18/Duality-ai.git](https://github.com/HarshitMendiratta-18/Duality-ai.git)
cd Duality-ai

# Initialize environment
ENV_SETUP/setup_env.bat
conda activate EDU
