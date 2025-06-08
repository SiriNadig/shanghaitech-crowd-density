# Crowd Density Estimation using CSRNet (ShanghaiTech Part A)

This project implements a deep learning model to estimate crowd density from images using **CSRNet (Convolutional Neural Network for Crowd Counting)**. The system is trained on the **ShanghaiTech Part A dataset**, which consists of high-density crowd scenes. The output is a **heatmap overlay** indicating crowded zones.

---

## 🎯 Project Objective

To generate accurate **crowd density heatmaps** from still RGB images of dense crowds using deep convolutional networks. The final predictions help in identifying zones of congestion and understanding crowd flow patterns.

---

## 📚 Dataset Used

**Dataset**: [ShanghaiTech with People Density Map (Part A)](https://www.kaggle.com/datasets/tthien/shanghaitech-with-people-density-map)

### Folder Structure:

ShanghaiTech/
└── part_A/
├── train_data/
│ ├── images/ # Input JPEG images
│ └── ground-truth-h5/ # Density maps in .h5 format
├── test_data/
├── images/
└── ground-truth-h5/

> **Part A** features high-density crowd images (e.g., public gatherings, protests, stadiums).

---

## 🧠 Model Architecture

The project uses **CSRNet**, which is based on:
- **Frontend**: VGG-16 convolutional layers (pretrained on ImageNet)
- **Backend**: Dilated convolution layers to preserve spatial resolution
- **Output**: 2D density map estimating the number of people in an image

---

## 🔧 Installation & Setup

### ✅ Requirements

```bash
pip install torch torchvision kagglehub matplotlib h5py opencv-python

> 📌 Dataset download and preprocessing is handled automatically in the Colab notebook.
