# 🧠 CodeAlpha Internship — Machine Learning
## Task 3: Handwritten Character Recognition

![Python](https://img.shields.io/badge/Python-3.10-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.15-orange)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![Internship](https://img.shields.io/badge/CodeAlpha-Internship-purple)

A Convolutional Neural Network (CNN) that recognizes handwritten digits and
letters from images, built as part of the **CodeAlpha Machine Learning
Internship**.

---

## 📌 Project Overview

| | |
|---|---|
| **Task** | Task 3 — Handwritten Character Recognition |
| **Internship** | CodeAlpha — Machine Learning Track |
| **Objective** | Identify handwritten characters/digits from images |
| **Approach** | Image processing + Deep Learning (CNN) |
| **Datasets** | MNIST (digits) and EMNIST (digits + letters) |
| **Tech Stack** | Python, TensorFlow/Keras, scikit-learn, NumPy, Matplotlib, Seaborn |

Handwriting recognition is a classic computer vision problem with real-world
uses in postal mail sorting, bank cheque processing, digitizing handwritten
forms/notes, and as a stepping stone toward full OCR (Optical Character
Recognition) systems.

---

## 🎯 What This Project Does

1. Loads a dataset of labeled handwritten character images (MNIST digits, or
   EMNIST digits + letters).
2. Preprocesses the images (normalization, reshaping, one-hot label encoding).
3. Builds and trains a CNN to classify each image into its correct character.
4. Evaluates performance with precision, recall, F1-score, and a confusion
   matrix — not just raw accuracy.
5. Visualizes results (training curves, confusion matrix, sample predictions).
6. Supports predicting on a **custom, user-supplied image** — draw a
   character, photograph it, and the model will classify it.



---

## 🧩 Model Architecture

```
Input (28 × 28 × 1)
   │
   ├── Conv2D(32) → BatchNorm → Conv2D(32) → MaxPool → Dropout(0.25)
   │
   ├── Conv2D(64) → BatchNorm → Conv2D(64) → MaxPool → Dropout(0.25)
   │
   ├── Flatten → Dense(256) → BatchNorm → Dropout(0.5)
   │
   └── Dense(num_classes, activation="softmax")
```

- **Optimizer:** Adam
- **Loss:** Categorical Cross-Entropy
- **Regularization:** Batch Normalization + Dropout (prevents overfitting)
- **Callbacks:** Early Stopping + Learning Rate Reduction


---

## 📊 Results

| Dataset | Classes | Test Accuracy |
|---|---|---|
| MNIST (digits) | 10 | ~99% |
| EMNIST-balanced (digits + letters) | 47 | ~88–90% |

**Evaluation artifacts generated:**
- `training_curves.png` — accuracy & loss per epoch
- `confusion_matrix.png` — per-class error breakdown
- `classification_report.txt` — precision, recall, F1-score per class
- `sample_predictions.png` — visual check of correct vs. incorrect predictions

> Letters are harder than digits due to visual overlap between certain
> characters (e.g., 'O' vs '0', lowercase 'l' vs '1').

---

## 🔍 Key Learnings

- How CNNs use convolution + pooling to progressively extract visual
  features, from simple edges to full character shapes.
- Why accuracy alone is insufficient for classification tasks — precision,
  recall, F1-score, and confusion matrices reveal *which* classes a model
  struggles with.
- The role of Dropout and Batch Normalization in controlling overfitting.
- How data augmentation (rotation, shift, zoom) improves generalization to
  real-world handwriting variation.
- Practical image preprocessing: matching a new image's pixel convention
  (color inversion, resizing) to what the model was trained on.

---

## 🔮 Future Improvements

- Extend from single-character to **word/sentence recognition** using a
  **CRNN** (CNN + Bidirectional LSTM + CTC loss) for sequence modeling.
- Deploy the trained model as a web app (e.g., Streamlit/Flask) with a live
  drawing canvas.
- Experiment with transfer learning from larger pretrained vision models.

---

## 🛠️ Tech Stack

`Python` · `TensorFlow / Keras` · `scikit-learn` · `NumPy` · `Matplotlib` · `Seaborn` · `PIL`

---

## 🙌 Acknowledgements

- [CodeAlpha](https://www.codealpha.tech) for the internship opportunity and task.
- [MNIST Dataset](http://yann.lecun.com/exdb/mnist/) — Yann LeCun et al.
- [EMNIST Dataset](https://www.nist.gov/itl/products-and-services/emnist-dataset) — NIST.

---

## 👤 Author

**Raja Ganapathi M**
Machine Learning Intern @ CodeAlpha
📧 rajaganapathimaharajan@gmail.com · 🔗 [LinkedIn](https://www.linkedin.com/in/rajaganapathi-m) · 💻 [GitHub](https://github.com/RajaGanapathi-M)

---

## 📄 License

This project was created for educational purposes as part of the CodeAlpha
Internship Program.

---

### #codealpha #machinelearning #deeplearning #cnn #computervision #internship
