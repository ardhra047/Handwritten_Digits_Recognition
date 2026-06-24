# Handwritten Digit Classification (MNIST)

A machine learning & deep learning project that classifies handwritten digits (0–9) using the MNIST dataset. The project compares traditional ML models (Logistic Regression, KNN, SVM) against a Convolutional Neural Network (CNN) to identify the best-performing approach for image classification.

## 📌 Problem Statement

**Input:** An image of a handwritten digit
**Output:** A predicted number from 0 to 9

This is a:
- Computer Vision problem
- Supervised Learning task
- Multi-class Classification problem (10 classes)

## 📊 Dataset

The project uses the **MNIST dataset**:
- 28 × 28 pixel grayscale images
- Pixel intensity values range from 0 (black) to 255 (white)
- Thousands of labeled training and testing samples
- Balanced class distribution with no missing values

## 🗂️ Project Workflow

### 1. Data Analysis
- Inspected dataset shape and train/test split
- Visualized sample images
- Checked class distribution across digits (0–9)

### 2. Data Preprocessing
- **Normalization:** Scaled pixel values from [0, 255] to [0, 1] for faster, more stable training
- **Flattening:** Converted 28×28 images into 784-length 1D vectors for traditional ML models (note: this loses spatial structure, which CNNs preserve)

### 3. Model Building

| Model | Approach | Notes |
|---|---|---|
| Logistic Regression | Linear baseline classifier | Fast but limited for complex image patterns |
| K-Nearest Neighbors (KNN) | Similarity-based classification | Intuitive but slow and memory-heavy on large datasets |
| Support Vector Machine (SVM) | Margin-based decision boundaries | Handles non-linear patterns better, but slower to train |
| Convolutional Neural Network (CNN) | Deep learning with convolution + pooling | Best performer — automatically learns spatial features like edges and curves |

**CNN Architecture Overview:**
1. **Convolution Layer** – detects edges, strokes, and patterns
2. **Pooling Layer** – reduces dimensionality while retaining key features
3. **Flatten Layer** – converts feature maps to 1D
4. **Dense Layer** – outputs final classification (digit 0–9)

### 4. Model Evaluation
Models were evaluated using:
- Accuracy
- Precision, Recall, F1-score
- Confusion Matrix (to identify commonly confused digit pairs, e.g., 3 vs 5, 4 vs 9)

### 5. Model Comparison

| Model | Spatial Understanding | Performance |
|---|---|---|
| Logistic Regression | Weak | Low |
| KNN | Medium | Good but slow |
| SVM | Strong | Better |
| **CNN** | **Best** | **Highest accuracy** |

**Conclusion:** CNN outperforms traditional ML models because it preserves spatial structure and automatically extracts relevant features instead of treating the image as a flat list of numbers.

### 6. Prediction System
1. Take a new input image
2. Preprocess it (resize/normalize to match training format)
3. Feed it to the trained model
4. Output the predicted digit (0–9)

## ⚠️ Challenges & Solutions

| Challenge | Solution |
|---|---|
| High-dimensional data (784 features/image) | Normalization + CNN feature extraction |
| Traditional models underperform on images | Switched to CNN |
| Risk of overfitting | Pooling layers, controlled training epochs |
| High computational cost (SVM/KNN) | Parameter tuning, prioritized CNN for deployment |

## 🛠️ Tech Stack
- Python
- NumPy, Pandas
- Matplotlib / Seaborn (visualization)
- Scikit-learn (Logistic Regression, KNN, SVM, evaluation metrics)
- TensorFlow / Keras (CNN)

## 📈 Results Summary

CNN achieved the highest accuracy among all tested models by leveraging spatial feature extraction through convolution and pooling layers, making it the most suitable architecture for image-based classification tasks like MNIST digit recognition.

## 📝 Final Summary

This project focuses on classifying handwritten digits using machine learning and deep learning techniques. After preprocessing the MNIST dataset, multiple models were applied and compared. CNN achieved the best performance due to its ability to capture spatial features, making it the most suitable model for image classification tasks.


