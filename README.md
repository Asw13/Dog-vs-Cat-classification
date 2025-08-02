# 🐶🐱 Dog vs Cat Image Classification

This repository contains my solution for the [Dog vs Cat Classification](https://www.kaggle.com/competitions/dog-vs-cat-classification/data) Kaggle competition. The goal is to build a classifier that can distinguish between images of dogs and cats.

---

## 📁 Dataset

The dataset is available on Kaggle and contains:

- `train/` — 25,000 labeled images (cats and dogs)
- `test/` — 8,000 unlabeled images
- `sample_submission.csv` — required format for Kaggle submission

🔗 [Dataset Link](https://www.kaggle.com/competitions/dog-vs-cat-classification/data)

---

## 🧠 Models Used

### ✅ InceptionV3 (Keras / TensorFlow)
- **Framework**: TensorFlow / Keras
- **Approach**: Transfer Learning
- **Modifications**:
  - `include_top=False`
  - `GlobalAveragePooling2D`
  - Final `Dense(1, activation='sigmoid')` for binary classification
- **Loss**: Binary Crossentropy
- **Optimizer**: Adam

### ✅ MobileNetV3 Small (PyTorch)
- **Framework**: PyTorch
- **Approach**: Transfer Learning with fine-tuning
- **Modifications**:
  - Replaced classifier head for binary output
  - Used `nn.BCEWithLogitsLoss()` for training
- **Optimizer**: Adam

Both models were trained, validated, and compared for accuracy and performance.

---

## 🧪 Results

| Model             | Validation Accuracy | Notes                         |
|------------------|---------------------|-------------------------------|
| InceptionV3       | ~90.9%              | Fast convergence, good performance |
| MobileNetV3 Small | ~97.9.X%              | Lightweight, faster inference |

> Replace `XX.X%` with your actual results.

---

## 🛠️ How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/dog-vs-cat-classification.git
cd dog-vs-cat-classification
