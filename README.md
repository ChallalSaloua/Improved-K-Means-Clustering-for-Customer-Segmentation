# Improved K-Means Clustering for Customer Segmentation

## Overview

This project presents an enhanced version of the K-Means clustering algorithm designed to improve clustering quality, robustness, and stability for customer segmentation tasks. The proposed approach combines three complementary techniques:

* **K-Means++ Initialization** for intelligent centroid selection.
* **MAD-Based Outlier Weighting** (Median Absolute Deviation) for robust handling of anomalous data points.
* **Agent-Based Competition Mechanism** inspired by Multi-Agent Systems to reduce the impact of local minima and improve convergence stability.

The project was developed as part of a Data Mining course and evaluated on a real-world credit card customer dataset containing 8,950 clients described by 17 financial and behavioral attributes.

---

## Objectives

The main goals of this project are:

* Improve the clustering quality compared to standard K-Means.
* Reduce sensitivity to random centroid initialization.
* Increase robustness against outliers.
* Enhance clustering stability across multiple executions.
* Analyze the contribution of each improvement through an ablation study.

---

## Methodology

### 1. Data Preprocessing

The dataset undergoes several preprocessing steps:

* Missing value imputation using median values.
* Feature standardization with StandardScaler.
* Exploratory Data Analysis (EDA).
* Principal Component Analysis (PCA) for visualization.

### 2. K-Means++ Initialization

Instead of selecting initial centroids randomly, K-Means++ chooses them probabilistically based on distance, ensuring better cluster separation and reducing convergence to poor local minima.

### 3. MAD-Based Soft Weighting

Outliers are detected using the Median Absolute Deviation (MAD), a robust statistical measure. Rather than removing outliers, the algorithm assigns lower weights to anomalous points, preserving valuable information while reducing their influence.

### 4. Agent-Based Competition

Each centroid is modeled as an autonomous agent with:

* Perception of clustering quality.
* Memory of its best position.
* Decision-making capability.
* Exploration through controlled perturbations.

This mechanism introduces adaptive optimization behavior and improves clustering stability.

---

## Experimental Evaluation

The proposed algorithm was compared against classical K-Means using several clustering validation metrics:

* Silhouette Score
* Davies-Bouldin Index
* Calinski-Harabasz Index
* Within-Cluster Sum of Squares (WCSS)

Additional evaluations include:

* Robustness analysis over 50 independent runs.
* Ablation study of each component.
* Benchmarking on multiple datasets:

  * Credit Card Customers
  * Iris Dataset
  * Wine Dataset
  * Synthetic Blob Dataset

---

## Results

The enhanced K-Means achieved:

* **+9.9% improvement** in Silhouette Score.
* **1.8% reduction** in Davies-Bouldin Index.
* **4.4% lower standard deviation** across repeated runs.
* Improved cluster consistency and stability.

The ablation study demonstrated that **K-Means++ initialization** contributes the largest performance gain, while MAD weighting and the agent-based mechanism further improve robustness and reliability.

---

## Technologies Used

* Python
* NumPy
* Pandas
* Scikit-Learn
* Matplotlib
* Seaborn
* PCA
* Statistical Validation Metrics





## Key Contributions

* Enhanced K-Means clustering framework.
* Robust outlier handling using MAD weighting.
* Agent-inspired centroid optimization strategy.
* Comprehensive experimental validation.
* Reproducible customer segmentation pipeline.

---

## Future Work

Potential extensions include:

* Reinforcement Learning-based centroid adaptation.
* Inter-agent communication strategies.
* Robust Mahalanobis-distance outlier detection.
* Large-scale distributed clustering.
* Real-time customer segmentation systems.

---

## Author

**CHALLAL Saloua**
Master's Student in Artificial Intelligence and Virtual Modeling (MIV)
University of Science and Technology Houari Boumediene (USTHB)
