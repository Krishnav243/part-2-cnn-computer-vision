# Part 2: Computer Vision Problem Formulation and CNN Prototype

## Project Overview

This project focuses on building a basic Convolutional Neural Network (CNN) model for image classification.

The dataset contains four classes of images:

- Dent
- Normal
- Scratch
- Stain

The goal is to classify images into their correct category using a CNN model.

---

## Problem Identification

### Selected Problem Type: Image Classification

This dataset represents an **image classification problem** because:

- Each image belongs to one specific category.
- The model predicts one label for every image.
- There are four predefined classes:
  - dent
  - normal
  - scratch
  - stain

---

## Dataset Exploration

### Number of Classes

**4 Classes**

- Dent
- Normal
- Scratch
- Stain

### Number of Images Per Class

Each class contains:

- 120 images

Total images:

**480 images**

### Dataset Balance

The dataset is balanced because all classes contain an equal number of images.

### Image Dimensions

- Width: 96 pixels
- Height: 96 pixels
- Channels: 3 (RGB)

---

## Image Preprocessing

The following preprocessing steps were applied:

- Images resized to fixed size (96 × 96)
- Pixel normalization (0–255 → 0–1)
- Train-test split (80% training, 20% testing)

Data augmentation was not applied because the dataset was balanced and sufficient for a basic CNN model.

---

## CNN Model Architecture

The CNN model includes:

- Convolution Layer (Conv2D)
- ReLU Activation Function
- Max Pooling Layer
- Flatten Layer
- Dense Layer
- Output Layer (Softmax)

Loss Function:
- Sparse Categorical Crossentropy

Optimizer:
- Adam

---

## Model Training and Evaluation

### Training Details

- Epochs: 15
- Batch Size: 32

### Model Performance

- Test Accuracy: 85.42%
- Test Loss: 0.3269

### Outputs

Results are saved in:

```text
results/
├── accuracy_loss_curves.png
└── confusion_matrix.png
