# image-classification-cnn-transfer-learning
Comparative study of CNN architectures vs Transfer Learning (VGG19) for multi-class image classification — from scratch to 95%+ accuracy
# 🖼️ Image Classification — CNN from Scratch vs Transfer Learning

> Academic project — CNAM, Engineering degree in AI & Data Science (2023)

Comparative study of deep learning architectures for multi-class image classification on the **Wang dataset** (1,000 images, 10 categories). The project explores the full progression from a simple CNN to Transfer Learning with VGG19, highlighting the impact of architectural choices, regularization techniques, and pre-trained feature extraction.

---

## 📁 Dataset — Wang Image Collection

| Property | Value |
|----------|-------|
| Total images | 1,000 |
| Categories | 10 |
| Images per class | 100 |
| Train / Test split | 70% / 30% |

**Categories:** Bus, Horses, Dinosaurs, Elephants, Flowers, Mountains, Food, Beach, Monuments, Jungle

---

## 🧪 Experiments & Results

### Progressive CNN Architecture Study

| Model | Key Features | Test Accuracy |
|-------|-------------|---------------|
| CNN Simple | 1 Conv layer, SGD | ~20% |
| CNN + Early Stopping | 1 Conv layer, patience=10 | ~53% |
| CNN Deeper | 3 Conv layers, Dropout, Adam | **75%** |
| CNN + Data Augmentation | Rotation, zoom, flip, shear | **83.7%** |
| **Transfer Learning VGG19** | Pre-trained ImageNet weights | **~95%+** |

### Key Findings

- **Data augmentation alone** boosted accuracy from 75% to 83.7% (+8.7 points) without changing the architecture
- **Transfer Learning with VGG19** massively outperforms any CNN trained from scratch, reaching 95%+ with only 25 epochs vs 50 for CNN models
- **Early stopping** prevents overfitting effectively but alone cannot compensate for a shallow architecture
- The gap between CNN from scratch (83.7%) and Transfer Learning (95%+) demonstrates the power of **pre-trained feature representations on ImageNet**

---

## 📂 Notebooks

| Notebook | Description |
|----------|-------------|
| `perceptron_simple_multiple.ipynb` | Baseline — simple and multi-layer perceptron |
| `Full Connected.ipynb` | Fully-connected network (no convolutions) |
| `CNN.ipynb` | Progressive CNN study — 4 architectures compared |
| `Transfert Learning.ipynb` | Transfer Learning with VGG19 pre-trained on ImageNet |

---

## 🛠️ Stack

![Python](https://img.shields.io/badge/-Python-3776AB?style=flat&logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/-TensorFlow-FF6F00?style=flat&logo=tensorflow&logoColor=white)
![Keras](https://img.shields.io/badge/-Keras-D00000?style=flat&logo=keras&logoColor=white)
![OpenCV](https://img.shields.io/badge/-OpenCV-5C3EE8?style=flat&logo=opencv&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/-Scikit--learn-F7931E?style=flat&logo=scikitlearn&logoColor=white)
![NumPy](https://img.shields.io/badge/-NumPy-013243?style=flat&logo=numpy&logoColor=white)

**Architectures:** CNN (Conv2D, MaxPooling, Dropout), VGG19 (Transfer Learning), Perceptron  
**Techniques:** Data augmentation (rotation, zoom, flip, shear), Early stopping, ImageDataGenerator  
**Evaluation:** Confusion matrix, Classification report, F1-score, Training curves

---

## 💡 Concepts Covered

- **Convolutional Neural Networks** — building blocks, receptive fields, feature maps
- **Regularization** — Dropout, Early Stopping, Data Augmentation
- **Transfer Learning** — feature extraction with frozen pre-trained weights (VGG19/ImageNet)
- **Hyperparameter tuning** — learning rate, batch size, optimizer (SGD vs Adam)
- **Evaluation** — multi-class confusion matrix, per-class precision/recall/F1

---

*This project was completed as part of the CNAM Engineering degree in AI & Data Science. It established a solid foundation in deep learning for image classification, directly informing current work on medical imaging models (skin lesion classification, tissue segmentation) in the [Empathy Health](https://github.com/walidsynoud/empathy-health) project.*
