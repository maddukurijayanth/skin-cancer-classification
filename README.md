# Skin Cancer Classification Using Hybrid Feature Fusion

## 📌 Project Overview

This project presents a **hybrid feature fusion approach for multi-class skin cancer classification** using real-world dermoscopic image datasets. The system combines deep learning features, transformer-based features, and handcrafted texture features to create a comprehensive representation of skin lesions.

The project uses **EfficientNetB0**, **Swin Transformer**, and **Gray-Level Co-occurrence Matrix (GLCM)** for feature extraction. The extracted features are fused and optimized using **Principal Component Analysis (PCA)**, while **SMOTE** is used to handle class imbalance. Finally, **XGBoost** and **LightGBM** are used for multi-class classification.

---

## 🎯 Problem Statement

Skin cancer classification from dermoscopic images is challenging because different skin lesion types can have similar visual characteristics. Medical image datasets may also suffer from significant class imbalance.

The objective of this project is to build a classification pipeline that combines complementary features from multiple feature extraction techniques for effective multi-class skin lesion classification.

---

## 📊 Datasets

The project uses real-world skin lesion data from:

- **HAM10000 Dataset**
- **ISIC 2019 Dataset**

The following metadata and ground-truth files are included in this repository:

- `HAM10000_metadata.csv`
- `ISIC_2019_Training_GroundTruth.csv`
- `ISIC_2019_Training_Metadata.csv`

> **Note:** The complete dermoscopic image datasets are not included in this repository due to their large size.

---

## 🔄 Methodology

The overall pipeline follows these steps:

1. Data preprocessing and metadata preparation
2. Dermoscopic image preprocessing
3. Deep feature extraction using **EfficientNetB0**
4. Transformer-based feature extraction using **Swin Transformer**
5. Handcrafted texture feature extraction using **GLCM**
6. Fusion of extracted features
7. Feature scaling
8. Dimensionality reduction using **PCA**
9. Handling class imbalance using **SMOTE**
10. Multi-class classification using **XGBoost and LightGBM**
11. Model evaluation and analysis

---

## 🧠 Feature Extraction Techniques

### EfficientNetB0

EfficientNetB0 is used as a convolutional neural network feature extractor to capture spatial patterns, lesion structures, colors, and other visual characteristics from dermoscopic images.

### Swin Transformer

Swin Transformer is used to extract transformer-based features and capture local and broader contextual relationships within skin lesion images.

### GLCM

Gray-Level Co-occurrence Matrix (GLCM) is used to extract handcrafted texture features describing properties such as:

- Contrast
- Correlation
- Energy
- Homogeneity

---

## 🔗 Feature Fusion and Optimization

Features extracted from **EfficientNetB0**, **Swin Transformer**, and **GLCM** are combined into a unified feature representation.

The fused features are then processed using:

- **Feature Scaling** for normalization
- **PCA** for dimensionality reduction
- **SMOTE** for handling class imbalance in the training data

---

## 🤖 Classification Models

### XGBoost

XGBoost is used for multi-class skin lesion classification based on the optimized fused feature representation.

### LightGBM

LightGBM is also used as a classification model to evaluate the effectiveness of gradient boosting on the fused feature set.

---

## 🛠️ Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- OpenCV
- TensorFlow
- PyTorch
- timm
- Scikit-learn
- imbalanced-learn
- XGBoost
- LightGBM
- Jupyter Notebook

---

## 📁 Project Structure

```text
skin-cancer-classification/
│
├── data/
│   ├── HAM10000_metadata.csv
│   ├── ISIC_2019_Training_GroundTruth.csv
│   └── ISIC_2019_Training_Metadata.csv
│
├── models/
│   ├── xgb_skin_cancer_model.pkl
│   ├── lgbm_skin_cancer_model.pkl
│   ├── pca.pkl
│   ├── scaler.pkl
│   └── label_encoder.pkl
│
├── notebooks/
│   ├── skin-cnacer-xgboost-lightgbm (13).ipynb
│   ├── app_ (13).ipynb
│   └── app_.ipynb
│
└── README.md
```

---

## 💾 Saved Models and Preprocessing Components

The `models/` directory contains trained models and preprocessing components required for inference:

| File | Description |
|---|---|
| `xgb_skin_cancer_model.pkl` | Trained XGBoost classification model |
| `lgbm_skin_cancer_model.pkl` | Trained LightGBM classification model |
| `pca.pkl` | Saved PCA dimensionality reduction model |
| `scaler.pkl` | Saved feature scaler |
| `label_encoder.pkl` | Saved label encoder for class labels |

---

## 📚 Key Learnings

Through this project, I gained practical experience in:

- Working with real-world medical imaging datasets
- Image preprocessing and metadata analysis
- Deep feature extraction using CNN architectures
- Transformer-based image feature extraction
- Handcrafted texture feature extraction using GLCM
- Fusion of features from multiple feature extractors
- Dimensionality reduction using PCA
- Handling imbalanced datasets using SMOTE
- Multi-class classification using XGBoost and LightGBM
- Saving trained models and preprocessing components for future inference

---

## ⚠️ Disclaimer

This project was developed for **academic and educational purposes only**. It is not intended for clinical diagnosis or medical decision-making.

---

## 👤 Author

**Jayanth Maddukuri**

GitHub: `maddukurijayanth`
