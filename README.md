# 🛣️ Offroad Terrain Segmentation - Duality AI

This project focuses on semantic segmentation for offroad environments using the **DINOv2** backbone. Developed during the Duality-ai hackathon.

## 📊 Model Performance
After 10 epochs of training on synthetic offroad data, the model achieved:
- **Final Validation Accuracy:** 70.29%
- **Mean IoU:** 0.2980
- **Dice Score:** 0.4434
- **Final Validation Loss:** 0.8165

## 📁 Project Structure
- `train_segmentation.py`: Main script for model training.
- `segmentation_head.pth`: Trained weights for the segmentation head.
- `train_stats/`: Contains training curves (Loss, Accuracy, IoU plots).
- `ENV_SETUP/`: Batch scripts for quick environment replication.

## 🛠️ Setup Instructions
1. Clone the repository: `git clone https://github.com/HarshitMendiratta-18/Duality-ai.git`
2. Run `ENV_SETUP/setup_env.bat` to create the environment.
3. Install dependencies: `pip install -r requirements.txt`

## 🚀 Next Steps
- Testing the model on real-world offroad images.
- Fine-tuning hyperparameters to improve the Mean IoU beyond the 0.2478 baseline.
-
