# Breast-cancer-classification-pytorch

## Overview

This project demonstrates an end-to-end deep learning workflow for breast cancer classification using PyTorch and the Wisconsin Breast Cancer Dataset.

The objective is to classify tumors as malignant or benign using 30 tumor-related features extracted from digitized images of breast masses.

The project covers:

* Data preprocessing
* Feature scaling
* Train-test splitting
* DataLoader implementation
* Neural network design
* Regularization techniques
* Model evaluation
* Model saving and loading
* Inference on unseen samples

---

## Dataset

Source:

Wisconsin Breast Cancer Dataset (available through Scikit-Learn)

Dataset characteristics:

* 569 patient samples
* 30 tumor measurement features
* Binary classification

Classes:

* 0 = Malignant
* 1 = Benign

---

## Model Architecture

Input Features: 30

Architecture:

30 → 64 → 32 → 2

Layers:

* Linear(30,64)
* BatchNorm1d(64)
* ReLU
* Dropout(0.3)
* Linear(64,32)
* ReLU
* Dropout(0.2)
* Linear(32,2)

Loss Function:

* CrossEntropyLoss

Optimizer:

* Adam
* Learning Rate = 0.001
* Weight Decay = 0.001

---

## Training Workflow

Dataset
→ StandardScaler
→ Train/Test Split
→ TensorDataset
→ DataLoader
→ Neural Network
→ Forward Pass
→ Loss Computation
→ Backpropagation
→ Weight Updates
→ Evaluation

---

## Performance

Results obtained:

* Accuracy: 97.37%
* Precision: 97.26%
* Recall: 98.61%
* F1 Score: 97.93%

Confusion Matrix:

[[40, 2],
[ 1,71]]

The model demonstrated strong predictive performance on unseen test samples while maintaining excellent recall and F1-score.

---

## Key Concepts Demonstrated

* Deep Learning with PyTorch
* Neural Network Design
* Batch Normalization
* Dropout Regularization
* Weight Decay
* Model Evaluation Metrics
* Model Persistence
* Inference Pipelines

---

## Future Improvements

* Hyperparameter tuning
* Cross-validation
* Early stopping
* ROC-AUC analysis
* Deployment as an API
* Application to RNA-seq classification datasets

---

## Author

Adekunle Ajiboye

Computational Biologist | Bioinformatics | Machine Learning | Deep Learning
