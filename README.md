# Skin-Cancer-EDA
# 🔬 Skin Cancer Detection — Exploratory Data Analysis

![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=flat&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat&logo=jupyter&logoColor=white)
![License](https://img.shields.io/badge/License-CC0%201.0-green?style=flat)
![Dataset](https://img.shields.io/badge/Dataset-ISIC-blue?style=flat)
![Images](https://img.shields.io/badge/Images-2357-orange?style=flat)
![Classes](https://img.shields.io/badge/Classes-9-purple?style=flat)

> A comprehensive Exploratory Data Analysis (EDA) of the ISIC Skin Cancer dataset, covering class distribution, train/test splits, class imbalance, and visual insights across 9 oncological disease categories.

---

## 📌 Table of Contents

- [About the Project](#about-the-project)
- [Dataset Overview](#dataset-overview)
- [Disease Classes](#disease-classes)
- [Dashboard Preview](#dashboard-preview)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Running in Google Colab](#running-in-google-colab)
- [EDA Highlights](#eda-highlights)
- [Key Findings](#key-findings)
- [Technologies Used](#technologies-used)
- [License](#license)

---

## 📖 About the Project

Melanoma is one of the deadliest forms of skin cancer, accounting for **75% of all skin cancer deaths**. Early detection is critical — a solution that can evaluate dermoscopic images and alert dermatologists to the presence of melanoma has the potential to drastically reduce manual diagnosis effort and save lives.

This project performs a thorough **Exploratory Data Analysis (EDA)** on the ISIC Skin Cancer dataset to understand the data distribution, class imbalance, and visual characteristics before any model training takes place.

---

## 📊 Dataset Overview

| Property | Details |
|---|---|
| **Source** | International Skin Imaging Collaboration (ISIC) |
| **Total Images** | 2,357 |
| **Classes** | 9 disease categories |
| **Train Split** | ~1,880 images (~80%) |
| **Test Split** | ~477 images (~20%) |
| **Image Format** | JPEG / PNG |
| **License** | CC0: Public Domain |
| **Usability Score** | 6.88 / 10 (Kaggle) |

The dataset was curated from ISIC and all images were sorted according to ISIC classifications. All subsets were divided into approximately equal numbers, with the exception of **Melanoma** and **Nevus**, whose images are slightly dominant.

---

## 🏷️ Disease Classes

The dataset contains images across the following **9 oncological conditions**:

| # | Disease | Type |
|---|---|---|
| 1 | **Melanoma** | Malignant |
| 2 | **Nevus** | Benign |
| 3 | **Pigmented Benign Keratosis** | Benign |
| 4 | **Basal Cell Carcinoma** | Malignant |
| 5 | **Actinic Keratosis** | Pre-malignant |
| 6 | **Seborrheic Keratosis** | Benign |
| 7 | **Squamous Cell Carcinoma** | Malignant |
| 8 | **Dermatofibroma** | Benign |
| 9 | **Vascular Lesion** | Benign/Malignant |

---

## 🖥️ Dashboard Preview

An interactive HTML EDA dashboard has been included in this repository. It features:

- 📊 Class distribution bar chart
- 🥧 Class share doughnut chart
- 📏 Class imbalance horizontal bars with mean line
- 🔵🔴 Train / Test split per class
- 📋 Dataset summary statistics table
- 🏷️ Color-coded disease class tags

👉 **[View Live Dashboard](./skin_cancer_eda_dashboard.html)**

---

## 📁 Project Structure

```
skin-cancer-eda/
│
├── 📓 skin_cancer_isic_eda.ipynb      # Main Colab-ready EDA notebook
├── 🐍 skin_cancer_eda.py              # Standalone Python EDA script
├── 🌐 skin_cancer_eda_dashboard.html  # Interactive HTML dashboard
├── 📄 README.md                       # This file
│
└── 📂 dataset/  (not included — download separately)
    ├── Train/
    │   ├── Melanoma/
    │   ├── Nevus/
    │   ├── Pigmented Benign Keratosis/
    │   ├── Basal Cell Carcinoma/
    │   ├── Actinic Keratosis/
    │   ├── Seborrheic Keratosis/
    │   ├── Squamous Cell Carcinoma/
    │   ├── Dermatofibroma/
    │   └── Vascular Lesion/
    └── Test/
        └── (same 9 class folders)
```

---

## 🚀 Getting Started

### Prerequisites

```bash
pip install numpy pandas matplotlib Pillow
```

### Run Locally

```bash
# Clone the repository
git clone https://github.com/Mukesh46-droid/skin-cancer-eda.git
cd skin-cancer-eda

# Download the dataset from Kaggle and place in ./dataset/

# Run the EDA script
python skin_cancer_eda.py
```

The script will automatically scan the `Train/` and `Test/` folders, count images per class, and generate a full EDA dashboard saved as `skin_cancer_eda_dashboard.png`.

---

## ☁️ Running in Google Colab

The easiest way to run this project is via Google Colab — no local setup required.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/your-username/skin-cancer-eda/blob/main/skin_cancer_isic_eda.ipynb)

**Steps:**
1. Click the badge above or upload `skin_cancer_isic_eda.ipynb` to [colab.research.google.com](https://colab.research.google.com)
2. Run **Cell 1** — imports all required libraries (pre-installed in Colab)
3. Run **Cell 2** — upload your dataset ZIP file via the file dialog
4. Run **Cell 3** — automatically scans folders and builds the dataset summary
5. Run **Cell 4** — generates and displays the full EDA dashboard
6. Run **Cell 5** — downloads the dashboard as a PNG image

> 💡 If you skip the upload step, the notebook will run on **simulated data** so you can still preview the dashboard.

---

## 📈 EDA Highlights

The notebook and dashboard cover the following analyses:

### 1. Class Distribution
Total image count per disease category, with percentage labels. Reveals which classes dominate the dataset.

### 2. Train / Test Split
Side-by-side comparison of training and testing image counts across all 9 classes. Confirms approximately 80/20 stratified split.

### 3. Class Imbalance Analysis
Horizontal bar chart sorted by image count with a mean line marker. Highlights the degree of imbalance between classes.

### 4. Sample Image Grid
One representative dermoscopic image displayed per class from the training set to give a visual understanding of each condition.

### 5. Summary Statistics Table
Key metrics including total images, train/test ratio, most/least common class, and imbalance ratio.

---

## 🔍 Key Findings

- **Melanoma** and **Nevus** are the most represented classes, reflecting their clinical prevalence.
- **Vascular Lesion** and **Dermatofibroma** have the fewest images, creating an imbalance ratio of approximately **5.4×**.
- The dataset has a consistent **80/20 train/test split**, with roughly 60 test images per class.
- **Class imbalance** is a significant concern — techniques such as data augmentation, oversampling (SMOTE), or weighted loss functions should be considered during model training.
- All images are sourced from ISIC and follow standardised dermoscopic imaging protocols, ensuring good image quality consistency.

---

## 🛠️ Technologies Used

| Tool | Purpose |
|---|---|
| **Python 3.8+** | Core programming language |
| **NumPy** | Numerical operations |
| **Pandas** | Data manipulation |
| **Matplotlib** | Static EDA charts and dashboard |
| **Pillow (PIL)** | Image loading and display |
| **Google Colab** | Cloud notebook environment |
| **Chart.js** | Interactive HTML dashboard charts |
| **HTML / CSS / JS** | Interactive web dashboard |

---

## 📚 References

- [ISIC Archive](https://www.isic-archive.com/) — International Skin Imaging Collaboration
- [Kaggle Dataset](https://www.kaggle.com/code/waelhlal/skin-cancer-detection-using-cnn) — Original dataset source
- [Skin Cancer Foundation](https://www.skincancer.org/) — Clinical background on melanoma

---

## 📄 License

This project is released under the **CC0 1.0 Universal (Public Domain)** license, consistent with the original ISIC dataset license.

You are free to use, modify, and distribute this work for any purpose without restriction.

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to open an issue or submit a pull request.

---

<div align="center">
  <p>Made with ❤️ for early cancer detection research</p>
  <p>⭐ Star this repo if you found it useful!</p>
</div>
