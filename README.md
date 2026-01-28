# Network Intrusion Detection using Machine Learning

## Overview
This project investigates machine learning approaches for **network intrusion detection**, a task
characterized by extreme class imbalance and high-dimensional feature spaces. The goal is to
distinguish benign network traffic from malicious activity while prioritizing reliable detection
of rare attacks.

Both supervised and unsupervised methods are explored, with model selection driven by empirical
performance rather than algorithmic complexity.

---

## Dataset
The dataset used in this project was obtained from Kaggle:

**`chethuhn/network-intrusion-dataset`**

It contains labeled network traffic records representing benign activity and multiple types of
network attacks. The data is composed primarily of numerical features extracted from network flows,
making it suitable for classification and anomaly detection tasks.

A defining characteristic of the dataset is its **severe class imbalance**, where benign traffic
dominates the observations. As a result, model evaluation focuses on recall and reliability for
attack detection rather than overall accuracy.

### Data Access
The dataset is downloaded programmatically using `kagglehub`.  
Instructions and usage are provided in the notebook.

---

## Objectives
- Detect malicious network activity from network flow features
- Evaluate model behavior under extreme class imbalance
- Compare supervised classification with unsupervised anomaly detection
- Emphasize recall for rare attack detection

---

## Methods

### Supervised Learning
- Random Forest classifier
- Dimensionality reduction using Principal Component Analysis (PCA)
- Standard feature scaling and careful train/test separation to avoid data leakage

### Unsupervised Learning
- Isolation Forest for anomaly detection, treating attacks as outliers

---

## Key Findings
- **Random Forest** demonstrated strong and stable performance in detecting malicious traffic,
  even under severe class imbalance.
- **Isolation Forest** struggled to reliably separate benign and malicious traffic, highlighting
  the limitations of purely unsupervised approaches in this context.
- Applying **PCA prior to supervised classification** reduced feature redundancy and improved
  model stability without significantly degrading performance.

---

## Final Model
The final approach combines:
- **Principal Component Analysis (PCA)** for dimensionality reduction
- **Random Forest** for classification

This combination offered the best balance between robustness, interpretability, and empirical
performance on rare attack detection.

---

## Evaluation
Model performance is assessed using:
- Precision, recall, and F1-score
- Confusion matrices
- Emphasis on recall for attack classes due to the high cost of false negatives

---

## Notes
This project prioritizes sound modeling decisions and evaluation practices over novelty. While
more complex models (e.g., gradient boosting) were considered, the final model was selected based
on observed performance and reliability rather than complexity.

---

## Author
Natalia Mirela De Lima  
Data Science student | Machine Learning | Network Security

