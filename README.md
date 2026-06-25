# 🩺 Hybrid IBR4Net-Swin Transformer for Skin Lesion Classification

## 📌 Overview

This project proposes a novel hybrid deep learning framework for multiclass skin lesion classification using dermoscopic images. The architecture combines **IBR4Net**, a lightweight CNN-based backbone for local feature extraction, with a **Swin Transformer** for capturing global contextual information. A **Bi-Directional Cross-Attention Fusion (BCAF)** mechanism is employed to effectively integrate features from both branches.

The model is trained and evaluated on the **ISIC 2019 Skin Lesion Dataset**, achieving an overall classification accuracy of **95.67%**.

---

## 🚀 Key Features

- Hybrid CNN-Transformer Architecture
- Custom **IBR4Net** Backbone
- **Swin Transformer** Global Feature Extraction
- Bi-Directional Cross-Attention Fusion (BCAF)
- Multi-Scale Attention-Based Feature Aggregation
- Two-Stage Progressive Training Strategy
- Focal Loss with Class Weighting
- Explainable AI using **Grad-CAM** and **LIME**
- State-of-the-Art Skin Lesion Classification Performance

---

## 🏗️ Architecture

### CNN Branch (IBR4Net)
- Inverted Bottleneck Residual Blocks
- Depthwise Separable Convolutions
- Squeeze-and-Excitation (SE) Attention
- Residual Connections

### Transformer Branch (Swin-T)
- Patch Embedding
- Window Multi-Head Self-Attention
- Shifted Window Attention
- Hierarchical Feature Learning

### Fusion Module
- Multi-Stage Feature Fusion
- Bi-Directional Cross-Attention
- Dynamic Feature Interaction
- Attention-Based Feature Aggregation

---

## 📊 Dataset

### ISIC 2019 Skin Lesion Dataset

The model is trained on the publicly available ISIC 2019 dataset containing dermoscopic images from multiple skin lesion categories.

**Dataset:** https://challenge.isic-archive.com/data/

### Classes
- Melanoma (MEL)
- Melanocytic Nevus (NV)
- Basal Cell Carcinoma (BCC)
- Actinic Keratosis (AK)
- Benign Keratosis (BKL)
- Dermatofibroma (DF)
- Vascular Lesion (VASC)
- Squamous Cell Carcinoma (SCC)

---

## ⚙️ Training Strategy

### Stage 1: Pretraining
- Input Resolution: 224 × 224
- Optimizer: AdamW
- Learning Rate: 1e-4
- Loss Function: Cross Entropy Loss

### Stage 2: Fine-Tuning
- Input Resolution: 384 × 384
- Learning Rate: 1e-5
- Loss Function: Focal Loss
- Class Weighting Enabled

---

## 🔍 Explainable AI (XAI)

### Grad-CAM
Visualizes important image regions influencing model predictions.

### LIME
Provides local explanations by highlighting significant image superpixels.

---

## 📈 Performance Comparison

| Model | Accuracy (%) |
|---------|---------|
| ResNet-50 | 89.8 |
| EfficientNet-B0 | 91.2 |
| IBR5Net | 92.1 |
| Swin-T | 92.6 |
| ConvNeXt-T | 93.1 |
| ConvNeXt-T + Swin-T | 94.3 |
| **IBR4Net-Swin-T (Proposed)** | **95.67** |

---

## 🧪 Ablation Study

| Configuration | Accuracy (%) |
|---------------|--------------|
| CNN Only | 87.2 |
| Swin Transformer Only | 89.1 |
| CNN + Swin Fusion | 90.3 |
| + Cross-Attention Fusion | 92.1 |
| + Feature Attention Fusion | 93.4 |
| + Two-Stage Training | 94.6 |
| + Focal Loss + Class Weights | **95.67** |

---

## 🛠️ Tech Stack

- Python
- TensorFlow / Keras
- NumPy
- Pandas
- OpenCV
- Scikit-Learn
- Matplotlib
- Grad-CAM
- LIME

---

## 🎯 Results

- Achieved **95.67% Classification Accuracy**
- Improved Local and Global Feature Learning
- Enhanced Performance on Imbalanced Classes
- Interpretable Predictions using Explainable AI
- Outperformed Conventional CNN and Transformer Models

---

## 🔮 Future Work

- Lightweight Architecture for Edge Deployment
- Mobile-Based Skin Lesion Diagnosis
- Integration of Clinical Metadata
- Semi-Supervised Learning
- Advanced Explainable AI Techniques

---

## 👨‍💻 Author

**Karan Kumar Gupta**

B.Tech Information Technology (2022-26)

---

## ⭐ Acknowledgements

- ISIC 2019 Challenge Dataset
- TensorFlow & Keras
- Swin Transformer Research Community
- Open Source AI Community
