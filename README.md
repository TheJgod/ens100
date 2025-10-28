# Industrial Wafer Defect Detection with CNNs and Anomaly Detection

## 📌 Overview

This repository implements an **end-to-end solution** for **industrial wafer defect detection** using **image classification** and **unsupervised anomaly detection**. The project tackles challenges like **highly imbalanced data**, **unseen drift classes**, and **asymmetric misclassification costs** by combining **ResNet-based CNNs**, **Teacher-Student networks**, and the **E"fficientAd anomaly detection framework**. 

**Custom penalty-weighted metrics** guide model training to prioritize correct detection of defective and anomalous parts.

**Key features**:  
- Supervised classification for **known defect types**  
- Unsupervised detection of **unknown anomalies (drift)**  
- Handling of **imbalanced datasets** through **upsampling** and **tailored loss functions**  
- **Data augmentation** and specialized training strategies for robust performance  
- **End-to-end inference pipeline** with **thresholding** for anomaly detection

---

## 📊 Dataset

The dataset comes from the **Valeo industrial quality control challenge** and consists of images of manufactured parts labeled for defects. Key characteristics include:

- **Classes**:
  - 🟢 1 class for **good parts**  
  - 🔴 6 classes for **different defect types** (e.g., Missing, Flat Loop, etc.)  
  - ⚠️ 1 **drift class** representing unknown anomalies (appears only in the test set)

- **Size**:
  - **Training set**: ~8,000 images  
  - **Test set**: ~1,000 images

- **Challenges**:
  - Highly **imbalanced classes**, with some defect types underrepresented  
  - **Variable inspection conditions** (different component types and inspection zones)  
  - Drift/unknown anomalies must be detected **unsupervised**, as they do not appear in the training set

- **Preprocessing & Augmentation**:
  - Normalization of image pixel values  
  - Rotation, translation, and cropping to increase variability and improve generalization  
  - Upsampling of underrepresented classes to mitigate class imbalance

---

## 🛠️ Setup

**Environment**:

```console
conda create -n erwan python=3.10
conda activate erwan
```

**Install packages**

```console
pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cpu
pip install scikit-learn scipy tqdm pillow matplotlib scikit-image pandas
```






