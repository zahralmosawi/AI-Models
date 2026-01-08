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

## Activities Classified
1. Walking
2. Sitting
3. Standing
4. Running
5. Cycling
6. Ascending stairs
7. Descending stairs
8. Jumping
9. Lying down
10. Rope jumping
11. Nordic walking
12. Ironing
13. Vacuum cleaning

## Methodology

### 1. Data Preparation
- Stratified sampling (5% of original dataset)
- Missing value imputation (mean for physiological features, forward/backward fill for orientation)
- Duplicate removal
- Outlier analysis (retained as valid extreme movements)
- Label encoding (13 activities → numeric labels 0-12)
- Feature scaling (StandardScaler)
- Train-test split (80-20, stratified)

### 2. Supervised Learning Models
Implemented and evaluated 6 classification algorithms:

| Model | Accuracy | Precision | Recall | F1-Score |
|-------|----------|-----------|--------|----------|
| **Random Forest** | **94.45%** | **94.87%** | **94.45%** | **94.39%** |
| Neural Network (MLP) | 92.81% | 92.83% | 92.81% | 92.79% |
| SVM (RBF, subset) | 88.07% | 88.47% | 88.07% | 87.86% |
| KNN (subset) | 86.19% | 86.54% | 86.19% | 85.96% |
| Logistic Regression | 66.79% | 66.95% | 66.79% | 65.73% |
| SVM (Linear) | 63.05% | 64.51% | 63.05% | 60.04% |

### 3. Hyperparameter Tuning
- Performed Grid Search for Logistic Regression
- Performed Randomized Search for Random Forest and Neural Network
- Tuned on stratified subsets (15k-30k samples)
- Used 3-fold cross-validation with F1-score optimization

### 4. Model Selection
**Random Forest** was selected as the optimal model due to:
- Highest accuracy (94.45%)
- Balanced precision and recall
- Fast training and prediction
- Robust to outliers
- Feature importance interpretability

## Key Findings
1. **Ensemble and deep learning methods significantly outperform linear models** for activity recognition from sensor data
2. **Random Forest provides the best balance** of accuracy, speed, and interpretability
3. **Non-linear patterns are essential** - linear models (Logistic Regression, Linear SVM) achieved only 63-67% accuracy
4. **Outliers represent valid extreme movements** during activities like jumping and should be retained

## Technologies Used
- **Language:** Python 3.12
- **Libraries:** 
  - scikit-learn (machine learning)
  - pandas (data manipulation)
  - numpy (numerical computing)
  - matplotlib & seaborn (visualization)
- **Environment:** Google Colaboratory

## Results & Visualizations
The notebook includes:
- Missing data heatmaps
- Box plots for outlier detection
- Class distribution charts
- Correlation heatmaps
- Confusion matrices for all models
- Model performance comparison tables

## Clinical Implications
This AI system enables hospitals to:
- ✅ Track patient compliance with prescribed exercises
- ✅ Detect deviations or abnormal movement patterns
- ✅ Adjust therapy protocols remotely based on patient performance
- ✅ Reduce need for constant in-person supervision
- ✅ Improve post-operative care and rehabilitation outcomes

## Limitations & Future Work
- **Dataset size:** Used 5% sample due to computational constraints
- **Hyperparameter tuning:** Tuned on subsets; full dataset tuning may improve performance
- **Real-time deployment:** Model needs optimization for edge devices
- **Feature engineering:** Additional domain-specific features could enhance accuracy

## Contributors
- Zahra Almosawi
- Rawan Mahmood
- Ahmed Abdulla
- Ali Matar
- Alaa Ahmed
- Esraa Alaradi

## License
This project is submitted as coursework for IT7009 at Bahrain Polytechnic.

---

**For detailed methodology, code implementation, and analysis, please refer to the Jupyter notebook.**
