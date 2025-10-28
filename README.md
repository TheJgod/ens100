# Industrial Wafer Defect Detection with CNNs and Anomaly Detection

## Overview

This repository implements an end-to-end solution for industrial wafer defect detection using image classification and unsupervised anomaly detection. The project tackles challenges like highly imbalanced data, unseen drift classes, and asymmetric misclassification costs by combining ResNet-based CNNs, Teacher-Student networks, and the E"cientAd anomaly detection framework. Custom penalty-weighted metrics guide model training to prioritize correct detection of defective and anomalous parts.

Key features: supervised classification for known defect types; unsupervised detection of unknown anomalies (drift), handling of imbalanced datasets through upsampling and tailored loss functions; data augmentation and specialized training strategies for robust performance; end-to-end inference pipeline with thresholding for anomaly detection.

## Dataset

The dataset comes from the **Valeo industrial quality control challenge** and consists of images of manufactured parts labeled for defects. Key characteristics include:

- **Classes**:
  - 1 class for **good parts**
  - 6 classes for **different defect types** (e.g., Missing, Flat Loop, etc.)
  - 1 **drift class** representing unknown anomalies (appears only in the test set)

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

## Environment Setup
```console
mkdir -p ~/miniconda3
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
rm ~/miniconda3/miniconda.sh
```

After installing, close and reopen your terminal application or refresh it by running the following command:

```console
source ~/miniconda3/bin/activate
conda init --all
```

## Create Environment:

```console
conda create -n erwan python=3.10
conda activate erwan
```

```console
conda create -n erwan python=3.10
conda activate erwan
```

## To Run Jupyter Notebook 

```console
pip install notebook
```

---
```console
sudo apt-get install wget gpg
wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
sudo install -D -o root -g root -m 644 packages.microsoft.gpg /etc/apt/keyrings/packages.microsoft.gpg
echo "deb [arch=amd64,arm64,armhf signed-by=/etc/apt/keyrings/packages.microsoft.gpg] https://packages.microsoft.com/repos/code stable main" |sudo tee /etc/apt/sources.list.d/vscode.list > /dev/null
rm -f packages.microsoft.gpg
```

```console
sudo apt install apt-transport-https
sudo apt update
sudo apt install code # or code-insiders
```
---

Make sure to install the python and jupyter extensions in vs code, just go to the extentions tab.

Select the Kernel after this.

## Install packages

```console
pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cpu
pip install scikit-learn scipy tqdm pillow matplotlib scikit-image pandas
```

## Github

Check First if it's already installed

```console
git version
```

If not, install it:

```console
sudo apt-get update
sudo apt-get install git-all
```

**Clone**

```console
git clone https://github.com/samyuktsriram/ens100.git
git config user.email "sriramsamyukt@gmail.com"
git config --global user.name "samyuktsriram"
```

Activate Conda Environment

```console
conda activate /mnt/disks/location/conda/envs/shared_env
```















