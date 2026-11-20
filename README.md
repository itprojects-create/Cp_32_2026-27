# Robust Underwater Monocular Depth Estimation

## 📌 Project Overview
Underwater environments present significant challenges for computer vision due to poor visibility, light absorption, scattering, color distortion, and suspended particles. These conditions reduce image quality and make depth estimation difficult.

This project focuses on **Robust Underwater Monocular Depth Estimation**, which predicts the depth of objects and scene elements from a single underwater RGB image using deep learning.

The objective is to develop, train, and evaluate deep learning models that estimate depth maps from underwater images and compare their performance using standard depth-estimation metrics.

---

## 🎯 Objectives

- Estimate depth from a single underwater RGB image.
- Investigate the challenges of underwater image degradation.
- Train and evaluate deep learning architectures for dense depth prediction.
- Compare different architectures based on their performance.
- Explore the generalization capability of models across different underwater datasets.
- Evaluate predicted depth maps using quantitative metrics and visual results.

---

## 🧠 Models and Architectures

The project explores different deep learning architectures for monocular depth estimation.

### 1. CNN (Convolutional Neural Network)
A baseline CNN model is used to learn spatial features from underwater images and predict dense depth maps.

### 2. MobileNetV2
MobileNetV2 is used as a lightweight feature extraction backbone. Its inverted residual blocks and depthwise separable convolutions provide efficient feature extraction with reduced computational cost.

### 3. YOLO-Based Depth Estimation
A pretrained YOLO backbone is explored for feature extraction. A custom decoder is added to transform extracted features into a dense depth map.

> YOLO is used as a feature extractor for depth prediction rather than solely for object detection.

---

## 📂 Datasets

### SQUID Dataset
The SQUID dataset is used for underwater image-based depth estimation experiments. It provides underwater imagery along with depth-related ground truth for supervised model training and evaluation.

### UV Multi Dataset
The UV Multi dataset is used for additional underwater depth-estimation experiments and dataset exploration. It helps investigate model performance under different underwater visual conditions.

Dataset preprocessing includes:
- Image resizing
- Depth-map preprocessing
- Valid-pixel masking
- Data loading and batching
- Preparation of training and validation datasets

---

## ⚙️ Project Workflow

1. Dataset collection and preparation
2. Image and depth-map preprocessing
3. Train-validation data loading
4. Model architecture implementation
5. Feature extraction
6. Dense depth-map prediction
7. Model training and validation
8. Performance evaluation
9. Depth-map visualization
10. Architecture comparison

---

## 📊 Evaluation Metrics

The models are evaluated using the following metrics:

| Metric | Description |
|---|---|
| **MSE** | Mean Squared Error between predicted and ground-truth depth |
| **RMSE** | Root Mean Squared Error; measures prediction error in depth units |
| **MAE** | Mean Absolute Error between predicted and actual depth |
| **Abs Rel** | Mean absolute error relative to ground-truth depth |
| **Delta 1 (δ < 1.25)** | Percentage of predictions within a factor of 1.25 of the ground truth |
| **Delta 2 (δ < 1.25²)** | Percentage of predictions within a factor of 1.25² of the ground truth |
| **Delta 3 (δ < 1.25³)** | Percentage of predictions within a factor of 1.25³ of the ground truth |

Lower values are better for MSE, RMSE, MAE, and Abs Rel. Higher values are better for Delta 1, Delta 2, and Delta 3.

---

## 🛠️ Technologies Used

- Python
- PyTorch
- Torchvision
- NumPy
- OpenCV
- Matplotlib
- Google Colab
- Ultralytics YOLO
- Jupyter Notebook

---

## 📈 Expected Outcome

- Dense depth maps generated from underwater RGB images.
- Quantitative evaluation of different deep learning models.
- Comparison between CNN, MobileNetV2, and YOLO-based approaches.
- Visualization of predicted depth maps.
- Analysis of model limitations under underwater visibility conditions.

---

## 🚀 Project Status

**Status:** Ongoing Research & Development

The project involves experimentation with different model architectures, training strategies, datasets, and evaluation methods to improve underwater monocular depth estimation performance.

---

## 👥 Project Repository

This repository contains the notebooks, implementations, experiments, and resources related to underwater monocular depth estimation.

