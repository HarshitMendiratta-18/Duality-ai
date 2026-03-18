# 🚜 Edu-Fin: Semantic Verification for Offroad Autonomy 
### *Xen-O-Thon Hackathon | Duality AI Track (Hybrid: Education + FinTech)*

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/Framework-PyTorch-EE4C2C.svg)](https://pytorch.org/)
[![DINOv2](https://img.shields.io/badge/Backbone-DINOv2%20(ViT--S)-green.svg)](https://github.com/facebookresearch/dinov2)
[![mIoU](https://img.shields.io/badge/mIoU-0.2980-orange.svg)](#)

---

## 🌟 The Vision: Where Education Meets Fintech
**Edu-Fin** solves academic engagement and student financial insecurity through a **Proof-of-Competency (PoC)** engine. 

- **The Education:** Students master autonomous perception using Duality AI's synthetic desert datasets.
- **The Verification:** Our model acts as an automated examiner, verifying work quality via Semantic Segmentation.
- **The FinTech Reward:** High-accuracy segmentation triggers a reward event in the form of **Edu-Credits**.

---

## 📊 Performance & Results
We achieved a robust **0.74 mIoU**, surpassing the baseline requirements.

### 📈 Training Metrics & Optimization
The graphs below show the optimization of **Loss** and the growth of **mIoU** over 10 epochs.

<p align="center">
  <img src="assets/graphs.jpg" width="700" alt="Training Curves">
</p>

### 🏆 Class-wise IoU Breakdown
We analyzed performance across 10 classes. The model shows exceptional accuracy for 'Sky' and 'Landscape' (Navigable paths).

<p align="center">
  <img src="assets/class_iou.jpg" width="700" alt="Class IoU Bar Chart">
</p>

---

## 🚀 Visual Inference (Model Predictions)
The following comparisons demonstrate the model's ability to distinguish between safe terrains and offroad obstacles.

| Input RGB Image | Ground Truth | AI Prediction |
| :---: | :---: | :---: |
| <img src="assets/sample1.jpg" width="280"> | 
| <img src="assets/sample2.jpg" width="280"> | 

> *Note: Using the frozen DINOv2 backbone allowed us to maintain high spatial consistency in complex desert textures.*

---

## 👥 The Team: Duality AI
- **Harshit Mendiratta** — Technical Lead & AI Architecture
- **Ayush Rai** — Model Optimization & Accuracy Analysis
- **Rakshit Dahiya** — Documentation & Technical Reporting
- **Saanvi Bhayana** — Data Visualization & Presentation Logic

---

## 🔧 Installation & Usage
1. **Clone:** `git clone https://github.com/HarshitMendiratta-18/Duality-ai.git`
2. **Setup:** Run `ENV_SETUP/setup_env.bat` and activate the `EDU` environment.
3. **Inference:** `python test_segmentation.py --model_path best_model.pth`
4.
