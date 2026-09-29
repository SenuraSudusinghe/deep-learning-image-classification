# Natural Scene Image Classification Using Deep Learning Models

## SE4050 – Deep Learning Assignment

A comparative study of four deep learning architectures for natural scene image classification using the Intel Image Classification Dataset.

---

## Project Overview

This project implements and evaluates four deep learning architectures for classifying natural scene images into six categories:

- Buildings
- Forest
- Glacier
- Mountain
- Sea
- Street

The objective is to compare model performance, computational efficiency, model complexity, and generalization capability under identical experimental conditions.

---

## Implemented Models

### 1. Simple CNN
Baseline convolutional neural network for scene classification.

### 2. Deep CNN
A deeper convolutional architecture designed to learn more complex visual representations.

### 3. VGG16 Transfer Learning
Pretrained VGG16 feature extractor with a custom classification head.

### 4. MobileNetV2 Transfer Learning
Pretrained MobileNetV2 feature extractor with a custom classification head.

---

## Dataset

### Intel Image Classification Dataset

Source:
https://www.kaggle.com/datasets/puneet6060/intel-image-classification

Classes:

| Class | Description |
|---------|---------|
| Buildings | Urban structures |
| Forest | Woodland scenes |
| Glacier | Snow and glacier environments |
| Mountain | Mountain landscapes |
| Sea | Coastal and ocean scenes |
| Street | Roads and street environments |

---

## System Architecture

The project follows the pipeline below:

Dataset
↓
Data Validation & EDA
↓
Image Preprocessing
↓
Data Augmentation
↓
Train / Validation / Test Split
↓
Model Training
↓
Model Evaluation
↓
Comparative Analysis

---

## Repository Structure

```text
deep-learning-image-classification/

├── notebooks/
│   ├── cnn.ipynb
│   ├── deep_cnn.ipynb
│   ├── vgg16.ipynb
│   └── mobilenetv2.ipynb
│
├── models/
│   ├── cnn/
│   ├── deep_cnn/
│   ├── vgg16/
│   └── mobilenetv2/
│
├── figures/
│
├── results/
│
├── reports/
│
├── requirements.txt
│
└── README.md
```

---

## Data Preprocessing

### Image Resizing

Input image size:

```python
224 x 224
```

### Normalization

```python
pixel = pixel / 255.0
```

### Data Augmentation

The following augmentation techniques were applied to training data:

- Random Horizontal Flip
- Random Rotation
- Random Zoom
- Random Translation

No augmentation was applied to the test dataset.

---

## Training Configuration

Framework:

```text
TensorFlow / Keras
```

Environment:

```text
Google Colab
```

Hardware:

```text
NVIDIA Tesla T4 GPU
```

Loss Function:

```python
SparseCategoricalCrossentropy
```

Optimizer:

```python
Adam
```

Batch Size:

```python
32
```

Epochs:

```python
10
```

---

## Evaluation Metrics

Each model was evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix
- Training Time
- Validation Performance
- Test Performance

---

## Running the Project

### Clone Repository

```bash
git clone <repository_url>
cd deep-learning-image-classification
```

### Run Notebooks

Open Jupyter Notebook or Google Colab and execute:

```text
cnn.ipynb
deep_cnn.ipynb
vgg16.ipynb
mobilenetv2.ipynb
```

---

## Example Prediction

Input:

```text
forest.jpg
```

Output:

```text
Forest – 98.3% Confidence
```

---

## Experimental Outputs

Generated outputs include:

- Training Curves
- Validation Curves
- Confusion Matrices
- Classification Reports
- Sample Predictions
- Comparative Analysis Tables

---

## Team Members

| Member | Responsibility |
|----------|----------|
| Senura Sudusinghe | MobileNetV2 & Integration |
| Evindu Ishen | Simple CNN |
| Mineth Perera | Deep CNN |
| Oshada Fernando | VGG16 & Evaluation |

---

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Pandas
- Matplotlib
- Scikit-Learn
- Google Colab
- GitHub

---

## References

1. Intel Image Classification Dataset
2. TensorFlow Documentation
3. Keras Documentation
4. MobileNetV2 Architecture Paper
5. VGG16 Architecture Paper

---

## License

This repository was developed as part of the SE4050 Deep Learning Assignment for academic purposes only.
