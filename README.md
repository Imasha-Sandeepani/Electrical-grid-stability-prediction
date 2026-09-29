# Machine Learning-Based Electrical Grid Stability Prediction

## Project Overview

This project develops machine learning classification models to predict
whether a decentralized electrical grid is **stable or unstable** based on
system characteristics such as reaction times, power consumption/production,
and price elasticity.

The objective is to explore how machine learning can support proactive grid
stability monitoring and help identify potentially unstable operating
conditions.

## Dataset

The project uses a decentralized smart grid stability dataset containing
**10,000 observations**.

The target variable is:

- `stabf` – Grid stability status (Stable / Unstable)

The predictive features include:

- Reaction times: `tau1`, `tau2`, `tau3`, `tau4`
- Power consumption/production: `p2`, `p3`, `p4`
- Price elasticity coefficients: `g1`, `g2`, `g3`, `g4`

## Machine Learning Workflow

The project follows an end-to-end machine learning workflow:

1. Data loading and exploration
2. Data preprocessing
3. Target variable encoding
4. Feature standardization
5. Exploratory Data Analysis (EDA)
6. Class imbalance analysis
7. Class balancing using SMOTE
8. Train-test splitting
9. Model training and evaluation
10. Feature importance analysis
11. Hyperparameter tuning
12. Model performance comparison

## Machine Learning Models

The following classification algorithms were evaluated:

- Logistic Regression
- Decision Tree
- Random Forest
- Support Vector Machine (SVM)

## Model Evaluation

Models were evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- AUC-ROC
- Confusion Matrix
- Training vs. Test Accuracy

The initial model comparison showed strong performance from Random Forest
and Support Vector Machine models.

### Initial Test Performance

| Model | Accuracy | Precision | Recall | AUC-ROC |
|---|---:|---:|---:|---:|
| Logistic Regression | 80.5% | 87.6% | 80.8% | 0.89 |
| Decision Tree | 85.5% | 89.3% | 87.8% | 0.85 |
| Random Forest | 92.6% | 92.3% | 96.3% | 0.98 |
| Support Vector Machine | 88.2% | 94.1% | 87.0% | 0.96 |

## Hyperparameter Tuning

Hyperparameter tuning was performed using **GridSearchCV with 5-fold
cross-validation**.

The tuned cross-validation accuracies were approximately:

- Logistic Regression: **81.4%**
- Decision Tree: **84.7%**
- Random Forest: **91.8%**
- Support Vector Machine: **95.8%**

The tuned SVM achieved the highest cross-validation accuracy among the
evaluated models.

## Key Insights

- The original target variable showed moderate class imbalance, with
  approximately 63.8% unstable and 36.2% stable observations.
- SMOTE was applied to the training data to balance the two classes.
- Reaction-time variables were important predictors of grid stability.
- Random Forest provided useful feature-importance information.
- Decision Tree showed signs of overfitting before tuning.
- Hyperparameter tuning improved model selection and generalization.
- SVM produced the highest cross-validation accuracy after tuning.

## Technologies & Libraries

- Python
- Pandas
- Scikit-learn
- Imbalanced-learn
- Matplotlib
- Seaborn
- NumPy
- Jupyter Notebook / Google Colab

## Repository Contents

- `ipynb file.ipynb` – Complete machine learning implementation
- `Report.pdf` – Detailed project report

## Academic Context

This project was completed as an individual assignment for the
Statistical & Machine Learning  module at the
University of Moratuwa.

