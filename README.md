# Predictive Alerting for Cloud Metrics

## Overview
This repository contains an end-to-end machine learning prototype for predicting cloud service incidents based on historical metrics. It was developed as a solution to a predictive alerting challenge, focusing on high recall and minimizing "alert fatigue" for DevOps teams.

## Key Technical Decisions
* **Synthetic Workload Generation:** Simulates realistic cloud CPU metrics, including daily seasonality, stochastic noise, and pre-incident degradation patterns (e.g., memory leaks).
* **Sliding Window Formulation:** Transforms continuous time-series data into a structured format suitable for supervised learning algorithms.
* **Chronological Data Splitting:** Ensures strict temporal separation between training and testing sets to prevent future data leakage.
* **Threshold Optimization:** Shifts away from standard accuracy metrics. Utilizes the Precision-Recall curve to find an optimal decision threshold, successfully achieving an **~80% incident detection rate (Recall)** while maintaining high **Precision (~88%)**.

## Tech Stack
* Python 3
* `pandas` & `numpy` (Data manipulation and windowing)
* `scikit-learn` (RandomForestClassifier and PR-curve evaluation)
* `matplotlib` (Visual analysis)

## How to Review
Simply open the `.ipynb` notebook file directly in GitHub to view the code, visualizations, and detailed architectural explanations.
