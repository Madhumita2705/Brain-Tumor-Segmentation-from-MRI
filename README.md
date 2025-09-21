Brain Tumor Segmentation – BraTS Dataset
**Overview**

This repository explores brain tumor segmentation from MRI scans using the BraTS dataset. The work is divided into phases, starting with baseline U-Net segmentation, then moving toward custom loss functions and advanced architectures for improved accuracy.

**📂 Dataset**

We use the BraTS Dataset:
🔗 https://www.kaggle.com/datasets/dschettler8845/brats-2021-task1/data

Multi-modal MRI scans (T1, T2, FLAIR, T1ce).

Expert-annotated tumor masks (whole tumor, core, enhancing regions).

Benchmark dataset for brain tumor segmentation research.

**Phase 1: Baseline Tumor Segmentation**

Dataset: BraTS MRI dataset with multi-modal brain scans (T1, T2, FLAIR, T1ce).

Data Preprocessing & Masking

  Multi-modal stacking: 4 MRI modalities (FLAIR, T1, T1ce, T2) combined into a 4-channel tensor.
  
  Mask-based normalization: Intensities normalized within brain region only (ignoring background).
  
  Patch sampling: Random 3D patches (128×128×128) taken, ensuring tumor presence.
  
  Augmentation: Random flips applied to both image & mask.

Model: Implemented a U-Net for pixel-level segmentation.


**Phase 2: Custom Loss Functions**

Hybrid Losses → combinations of Dice + Cross Entropy

**Phase 3: Advanced Architectures**

Attention U-Net → emphasizes tumor-relevant regions.


3D U-Net → captures volumetric context from MRI slices.

