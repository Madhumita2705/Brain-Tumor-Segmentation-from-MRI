# Brain Tumor Segmentation from MRI (BraTS Dataset)

This project implements **3D brain tumor segmentation** using MRI scans from the **BraTS 2021 dataset**. It establishes a baseline 3D U-Net model and then implements advanced experiments to improve the baseline model and comapares results.

## 📂 Dataset
- **Source:** [BraTS 2021 – Kaggle](https://www.kaggle.com/datasets)
- **Modalities:** T1, T1Gd, T2, FLAIR
- **Preprocessing:**
  - Normalization 
  - Random 64³ patch extraction with tumor inclusion
  - Data augmentation

## 🗺️ Project Roadmap

### Phase 1: Baseline Model ✅
`Phase_1_final_brain-tumor-segmentation-from-mri-brats-dataset .ipynb`
- **Model:** 3D U-Net (encoder-decoder)
- **Loss:** Standard Dice Loss
- **Training:**
- **Evaluation:** Mean Dice score on validation set

**Outcome:** Working 3D U-Net for tumor segmentation with a baseline performance benchmark.

### Phase 2: Advanced Experiments (Planned)
- Hybrid Loss: Dice + Cross-Entropy
- Boundary Loss: distance maps
- Attention U-Net

### Phase 3: Final Analysis
- Compute and visualize metrics for all experiments
