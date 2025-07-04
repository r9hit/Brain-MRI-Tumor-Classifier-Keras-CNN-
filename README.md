# Brain MRI Tumor Classifier (Keras + CNN)

A Convolutional Neural Network (CNN)-based deep learning model for classifying brain tumors in MRI images into four categories using the Brain Tumor Classification MRI dataset from Kaggle.

## 🧠 Overview

This project aims to assist in the early detection and classification of brain tumors by analyzing MRI scans with a custom-built CNN model. The model is trained to classify images into four tumor types with high accuracy, leveraging deep learning techniques in Keras.

## 📁 Dataset

- **Source:** [Kaggle - Brain Tumor Classification MRI Dataset](https://www.kaggle.com/datasets/sartajbhuvaji/brain-tumor-classification-mri)
- **Classes:** Glioma, Meningioma, Pituitary Tumor, No Tumor
- **Format:** RGB MRI images

## ⚙️ Preprocessing

- Resized images to **150x150** pixels
- Normalized pixel values to the range [0, 1]
- Applied data augmentation: rotation, flipping, zoom, contrast adjustment

## 🧱 CNN Architecture

- Built using Keras `Sequential` API
- Multiple Conv2D → ReLU → MaxPooling → Dropout blocks
- Fully connected Dense layers for classification
- Output layer: `Dense(4, activation='softmax')`

## 🧪 Training Details

- **Loss Function:** Categorical Crossentropy
- **Optimizer:** Adam
- **Metrics:** Accuracy
- **Epochs:** 20
- **Batch Size:** 32
- **Callbacks:** EarlyStopping, ModelCheckpoint

### 📈 Performance

| Epoch | Training Accuracy | Validation Accuracy |
|-------|-------------------|---------------------|
| 1     | 29.7%             | 28.4%               |
| 10    | 84.4%             | 73.9%               |
| 20    | **95.9%**         | **86.5%**           |

> The model demonstrated strong generalization with effective regularization and early stopping.

## 🖥️ Tech Stack

- Python
- Keras + TensorFlow backend
- NumPy, Pandas, Matplotlib
- Scikit-learn
- KaggleHub (for dataset access)

## 📊 Results

The model achieved:
- **95.9% training accuracy**
- **86.5% validation accuracy**
- Consistent convergence and reduced overfitting through dropout and augmentation

