# IDS
#  IntrusionDetection-NaiveBayes: IDS with PCA and KDD Cup 1999 Dataset

This project implements a machine learning-based Intrusion Detection System (IDS) using the **Naive Bayes algorithm** on the **KDD Cup 1999 dataset**. It classifies network connections as normal or one of several types of attacks, such as DoS, Probe, R2L, and U2R. The pipeline includes data preprocessing, dimensionality reduction using **PCA**, and classification using **Gaussian Naive Bayes**.

---

##  Project Overview

- **Objective:** Classify network traffic records into 6 major categories: `normal`, `dos`, `probe`, `r2l`, `u2r`, `other`.
- **Dataset:** [KDD Cup 1999](http://kdd.ics.uci.edu/databases/kddcup99/kddcup99.html) — used both training and test splits with a total of ~148,000 entries.
- **Approach:**
  - Preprocess and rebalance the dataset.
  - Perform one-hot encoding of categorical features.
  - Apply **MinMax Scaling** and **Principal Component Analysis (PCA)** to reduce dimensionality.
  - Train and evaluate a **Gaussian Naive Bayes** model.

---

##  Key Techniques

- **Data Cleaning & Label Mapping:** Group 37 raw labels into 6 broader categories.
- **Class Balancing:** Downsample frequent classes and upsample rare ones.
- **Dimensionality Reduction:** Reduce 120+ features to 10 principal components using **PCA**.
- **Classification:** Gaussian Naive Bayes (sklearn) used for final predictions.
- **Model Evaluation:**
  - Accuracy: **81.05%**
  - Precision, Recall, F1-Score
  - Confusion Matrix and Classification Report

---

## Libraries Used

- Python 3.7+
- `pandas`, `numpy`
- `matplotlib`, `seaborn`
- `sklearn` (PCA, Naive Bayes, preprocessing, metrics)

---

## File Structure

```bash
├── kdd_train.csv
├── kdd_test.csv
├── intrusion_detection_nb.ipynb  # Main Colab Notebook
