# 🌿 Plant Disease Detection Using Deep Learning

A deep learning project for **plant disease classification** using image-based computer vision.

The project compares different CNN architectures and transfer learning approaches to evaluate their performance on plant disease images.

---

## 🎯 Project Overview

The notebook evaluates five approaches:

- Baseline CNN
- Improved CNN
- CNN with Data Augmentation
- MobileNetV2
- EfficientNetB0

The models are trained and evaluated to compare their classification performance.

---

## 🗂️ Dataset

The dataset is obtained from **Kaggle** using the KaggleHub API.

The images are organized into folders according to their plant disease classes.

The dataset is analyzed through:

- Class distribution
- Dataset imbalance
- Sample images
- Image dimensions

Images are resized to **224 × 224** pixels for model training.

---

## 🔄 Data Preparation

The dataset is divided into:

- **80% Training**
- **10% Validation**
- **10% Testing**

Class weights are calculated and used during training to address class imbalance.

TensorFlow's Dataset API is used with prefetching for efficient data loading.

---

## 🧠 Models

### 1. Baseline CNN
A traditional CNN consisting of convolutional layers, max-pooling, flattening, and dense classification layers.

### 2. Improved CNN
An improved version of the baseline architecture using:

- Global Average Pooling
- A smaller dense layer
- Dropout

### 3. CNN + Data Augmentation
The baseline CNN is trained with data augmentation to evaluate its effect on classification performance.

### 4. MobileNetV2
A transfer learning model based on the pretrained **MobileNetV2** architecture.

### 5. EfficientNetB0
A transfer learning model based on pretrained **EfficientNetB0** weights.

---

## ⚙️ Training

| Parameter | Value |
|---|---|
| Image Size | `224 × 224` |
| Batch Size | 32 |
| Optimizer | Adam |
| Loss | Sparse Categorical Crossentropy |
| Class Weights | Yes |
| Early Stopping | Yes |
| Framework | TensorFlow / Keras |

---

## 📊 Results

The final evaluation on the test set produced the following results:

| Model | Test Accuracy | Test Loss |
|---|---:|---:|
| Baseline CNN | 93.60% | 0.1804 |
| Baseline + Augmentation | 93.71% | 0.1771 |
| MobileNetV2 | 95.00% | 0.1587 |
| Improved CNN | 96.52% | 0.1053 |
| EfficientNetB0 | 96.55% | 0.1285 |

The notebook also evaluates the models using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrices

---

## 🛠️ Technologies

- Python
- TensorFlow / Keras
- NumPy
- Pandas
- OpenCV / PIL
- Scikit-learn
- Matplotlib
- Seaborn
- KaggleHub
- Google Colab

---

## ▶️ How to Run

1. Open the notebook in **Google Colab**.
2. Import the dataset using KaggleHub.
3. Run the notebook cells sequentially.
4. The notebook performs dataset analysis, preprocessing, model training, and evaluation.
5. Compare the performance of the different models using the generated metrics and visualizations.

---

## 📌 Project Conclusion

The experiments compare traditional CNN architectures with transfer learning models for plant disease classification.

The reported test results show high classification accuracy across the evaluated models, with **EfficientNetB0 achieving 96.55% test accuracy**.

---

## 👥 Team

- **Chaima Mansouri**
- **Nour El Imene Houadji**
- **Chahd Touabia** 
