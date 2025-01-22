# Brain Scan Classification – Deep Learning Project
**Eylon Yehiel**

---
<div align="center">
  <img src="https://github.com/user-attachments/assets/eeeabb72-49db-4608-910b-dd1962a4b518" alt="giphy">
</div>


## Introduction
This project develops a deep learning system for automatic classification of brain tumors using MRI and CT scan images. Using convolutional neural networks (CNNs), the system explores multiple approaches, including models trained from scratch and transfer learning with VGG16. With a dataset of 9,618 images from Kaggle, the system achieved accuracy rates exceeding 95%. This project highlights the potential of deep learning in medical imaging diagnostics, particularly for tumor detection and classification.

Brain tumor detection and classification are crucial in medical diagnosis but often rely on expert interpretation of medical images. This manual process is time-consuming and prone to human error. This project addresses the challenge by developing an automated classification system using deep learning techniques.

---

## Motivation
1. Reduce human error in tumor detection.
2. Provide a reliable second-opinion tool for medical professionals.
3. Improve efficiency in medical image analysis.
4. Create a scalable solution for different types of medical imaging.

---

## Objectives
1. Develop accurate classification models for MRI and CT scan images.
2. Compare performance between models trained from scratch and transfer learning approaches.
3. Evaluate the impact of data augmentation on model performance.

---

## Dataset
- **Source**: [Kaggle](https://www.kaggle.com/datasets/murtozalikhon/brain-tumor-multimodal-image-ct-and-mri)
- **Images**: 9,599 total (4,981 MRI scans and 4,618 CT scans).
- **Labels**: Binary classification ("0" for healthy, "1" for disease).
- **Image Size**: 180x180 pixels, RGB format.
- **Split**:
  - Train: 64%
  - Validation: 16%
  - Test: 20%

---

## Methodology
### 1. **Models from Scratch**
- 5 Conv2D layers with increasing filters (32–256) and ReLU activation.
- MaxPooling2D layers for spatial reduction.
- Fully connected layer with sigmoid activation.
- Training: 30 epochs, batch size 30.

### 2. **Data Augmentation**
- Random horizontal flip, rotation, zoom, and brightness adjustment.
- Added dropout layers to prevent overfitting.
- Training: 100 epochs.

### 3. **Transfer Learning (VGG16)**
- **Feature Extraction**: Used the second-last layer of VGG16 with ImageNet weights.
- **Fine-Tuning**: Enabled training for the last 4 layers of the pretrained model.
- Added augmentation for enriched image representation.

### 4. **Evaluation Metrics**
- Accuracy, *precision*, recall, F1 score.
- Confusion matrix and classification report.
  
---

## Links
- **Project Repository**: [GitHub](https://github.com/EylonYehiel/Brain-Scan-Classification-Deep-Larning)
- **Data Source**: [Kaggle](https://www.kaggle.com/datasets/murtozalikhon/brain-tumor-multimodal-image-ct-and-mri)

---
