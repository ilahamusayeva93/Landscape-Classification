# Image Classification with CNN

## Overview

This script demonstrates the process of training a Convolutional Neural Network (CNN) for image classification using the Intel Image Classification dataset. The dataset consists of approximately 25,000 images of size 150x150, distributed across six categories: buildings, forest, glacier, mountain, sea, and street.

## Dataset Information

- **Dataset:** [Intel Image Classification](https://github.com/fafilia/cnn-intel_images)
- **Categories:**
  - 'buildings' (0)
  - 'forest' (1)
  - 'glacier' (2)
  - 'mountain' (3)
  - 'sea' (4)
  - 'street' (5)
- **Data Distribution:**
  - Train: ~14,000 images
  - Test: ~3,000 images
  - Prediction: ~7,000 images

## Script Structure

### 1. Data Preparation

- **Directory Setup:** Creates necessary directories for storing training and prediction images.

- **Data Download:** Clones the GitHub repository containing the dataset.

- **Data Loading:** Loads the data into PyTorch datasets using `ImageFolder`.

- **Data Splitting:** Splits the training dataset into training and validation sets.

### 2. Model Definition

- **Convolutional Neural Network (CNN):** Defines a simple CNN architecture for image classification.

- **Loss Function and Optimizer:** Specifies the CrossEntropyLoss as the loss function and Adam optimizer.

### 3. Model Training

- **Training Loop:** Iterates over epochs, trains the model, and prints loss at regular intervals.

- **Validation:** Evaluates the model on the validation set and saves the best model based on validation accuracy.

- **Early Stopping:** Implements early stopping if the model does not show improvement in validation accuracy.

### 4. Model Testing

- **Loading Best Model:** Loads the saved model with the best validation accuracy.

- **Test Accuracy:** Evaluates the model on the test set and prints the accuracy.

### 5. Unlabeled Image Prediction

- **Unlabeled Dataset:** Creates a dataset for unlabeled images to make PyTorch's `ImageFolder` work.

- **Prediction:** Uses the trained model to predict labels for unlabeled images.

- **Visualization:** Randomly selects images from the test set and compares true labels with predictions.

## How to Use

1. Run the script in a Python environment with PyTorch installed.

2. Ensure that the required directories are created.

3. Download the dataset from [Intel Image Classification](https://github.com/fafilia/cnn-intel_images) and place it in the appropriate folders.

4. Execute the script and follow the output for training and testing results.

## Author

- **Author:** Ilaha Musayeva
- **Date:** 20/20/2023


