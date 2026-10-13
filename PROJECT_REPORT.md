# Skin Cancer Detection — Project Report

## 1. Introduction

This project investigates multi-class skin-lesion image classification using deep learning and transfer learning.

## 2. Dataset

The HAM10000 dataset was obtained from Kaggle:

https://www.kaggle.com/datasets/kmader/skin-cancer-mnist-ham10000

The classification task includes seven categories: akiec, bcc, bkl, df, mel, nv, and vasc.

## 3. Data Preprocessing

- Matched metadata records with image files.
- Removed records with missing image paths or labels.
- Used stratified train, validation, and test splits.
- Resized images to 224 × 224 pixels.
- Applied MobileNetV2 preprocessing.
- Used class weights to address class imbalance.

## 4. Model Architecture

MobileNetV2 pretrained on ImageNet was used as a feature extractor. A classification head consisting of global average pooling, dropout, and a seven-unit softmax layer was added.

## 5. Training

The model was trained using the training set. Validation loss was monitored with early stopping, model checkpointing, and learning-rate reduction.

## 6. Evaluation Results

| Metric | Result |
|---|---:|
| Test Accuracy | 0.6574 |
| Macro F1-Score | 0.4612 |
| Weighted F1-Score | 0.6892 |
| Test Samples | 1503 |

Detailed class-wise results are available in `classification_report.csv`.

## 7. Limitations

- The dataset may not represent all populations or imaging conditions.
- Class imbalance may affect per-class performance.
- Dataset performance does not establish clinical diagnostic reliability.
- Further external validation would be required before any real-world medical use.

## 8. Conclusion

A MobileNetV2-based image classifier was trained to classify seven HAM10000 lesion categories. The model's measured test metrics and class-wise results provide an educational assessment of its performance on the held-out dataset.

## 9. Disclaimer

This project is for educational purposes only. It is not intended for medical diagnosis, screening, or treatment decisions.

## Author

Muhammad Abdullah
