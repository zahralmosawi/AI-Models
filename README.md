# AI Activity Classification Project

## Course Information
- **Course:** IT7009 - Artificial Intelligence
- **Institution:** Bahrain Polytechnic
- **Project Type:** Group Project

## Project Overview
This project develops an AI-based solution for monitoring patient recovery in hospitals using wearable sensor data. The system automatically classifies 13 different physical activities to help healthcare providers track patient compliance with prescribed exercises and detect abnormal movement patterns.

## Problem Statement
Multi-specialty hospitals in Bahrain are implementing digital transformation initiatives to automate recovery monitoring for patients with neurological disorders and elderly individuals with movement-related conditions. Traditional rehabilitation depends on correct exercise execution and consistency, which is difficult to monitor without in-person supervision.

## Solution
We developed machine learning models that analyze data from wearable Inertial Measurement Units (IMUs) worn on the wrist, chest, and ankle. These sensors capture:
- 3D Accelerometer data
- 3D Gyroscope data
- 3D Magnetometer data
- Heart rate
- Hand temperature
- Quaternion orientation

## Dataset
- **Source:** Wearable sensor recordings
- **Participants:** 9 individuals
- **Activities:** 13 physical activities
- **Features:** 23 numeric sensor measurements
- **Sampling:** Stratified 5% sample maintaining activity proportions

## Results

We implemented and evaluated 6 classification algorithms:

| Model | Accuracy | Precision | Recall | F1-Score |
|-------|----------|-----------|--------|----------|
| **Random Forest** | **94.45%** | **94.87%** | **94.45%** | **94.39%** |
| Neural Network (MLP) | 92.81% | 92.83% | 92.81% | 92.79% |
| SVM (RBF, subset) | 88.07% | 88.47% | 88.07% | 87.86% |
| KNN (subset) | 86.19% | 86.54% | 86.19% | 85.96% |
| Logistic Regression | 66.79% | 66.95% | 66.79% | 65.73% |
| SVM (Linear) | 63.05% | 64.51% | 63.05% | 60.04% |

**Random Forest** achieved the best performance with 94.45% accuracy and was selected as the final model.

## Technologies Used
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557c?style=for-the-badge&logo=python&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)

## Contributors
- Zahra Almosawi
- Rawan Mahmood
- Ahmed Abdulla
- Ali Matar
- Alaa Ahmed
- Esraa Alaradi

---

**Submitted for IT7009 - Artificial Intelligence**  
**Bahrain Polytechnic | December 2025**
```

---
