# Skin Cancer Detection Using Deep Learning

## Project Overview

This project uses transfer learning with MobileNetV2 to classify dermatoscopic skin-lesion images into seven categories from the HAM10000 dataset.

It demonstrates image preprocessing, deep learning, model evaluation, and reproducible machine-learning workflows.

## Objectives

- Explore and preprocess the HAM10000 dataset.
- Build a seven-class image classification model.
- Apply transfer learning with MobileNetV2.
- Evaluate the model using accuracy, precision, recall, and F1-score.
- Document the experiment for reproducibility.

## Dataset

**HAM10000 — Skin Cancer MNIST**

Kaggle: https://www.kaggle.com/datasets/kmader/skin-cancer-mnist-ham10000

The dataset contains dermatoscopic images across seven lesion categories.

| Label | Category |
|---|---|
| akiec | Actinic keratoses and intraepithelial carcinoma |
| bcc | Basal cell carcinoma |
| bkl | Benign keratosis-like lesions |
| df | Dermatofibroma |
| mel | Melanoma |
| nv | Melanocytic nevi |
| vasc | Vascular lesions |

## Model

- Architecture: MobileNetV2
- Approach: Transfer learning
- Input size: 224 × 224 × 3
- Output: 7-class softmax classifier
- Framework: TensorFlow / Keras

## Evaluation Results

| Metric | Result |
|---|---:|
| Test Accuracy | 0.6574 |
| Macro F1-Score | 0.4612 |
| Weighted F1-Score | 0.6892 |
| Test Samples | 1503 |

See `classification_report.csv` for per-class results and `confusion_matrix.png` for the confusion matrix.

## Project Files

- `Skin_Cancer_Detection.ipynb` — complete notebook
- `README.md` — project overview
- `PROJECT_REPORT.md` — technical report
- `requirements.txt` — Python dependencies
- `.gitignore` — ignored files
- `evaluation_metrics.csv` — overall evaluation metrics
- `classification_report.csv` — per-class metrics
- `training_history.csv` — training history
- `training_curves.png` — training plots
- `confusion_matrix.png` — confusion matrix

## How to Run

1. Open the notebook in Google Colab.
2. Install the dependencies listed in `requirements.txt`.
3. Download the dataset using KaggleHub.
4. Run the notebook cells in order.
5. Review the evaluation metrics and plots.

## Limitations and Disclaimer

This project is for educational and research purposes only. It is not a medical diagnostic system and must not be used to diagnose skin cancer or guide treatment.

Performance on HAM10000 does not establish clinical reliability or guarantee generalization to other populations, devices, or image sources.

## Author

Muhammad Abdullah  
Data Science Graduate | AI & Machine Learning
