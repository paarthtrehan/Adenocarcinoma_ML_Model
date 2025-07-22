Breast Cancer Diagnostic Prediction using Tree-Based Models
By Paarth Trehan

This project leverages the Wisconsin Breast Cancer Diagnostic Dataset to develop and compare several tree-based classification models for predicting whether a tumor is malignant or benign. The goal is to explore predictive modeling techniques and identify the most effective features and algorithms for accurate diagnosis.

Dataset Overview
Each data record corresponds to a fine needle aspirate (FNA) of a breast mass. The dataset includes:

Target variable: Diagnosis

M = Malignant

B = Benign

Features: 30 numerical measurements derived from 10 base attributes of each cell nucleus:

Radius, Texture, Perimeter, Area, Smoothness

Compactness, Concavity, Concave Points, Symmetry, Fractal Dimension

Each base feature includes:

Mean value

Standard error (SE)

Worst value (mean of 3 largest)

🛠️ Methodology
The project workflow included the following steps:

Data Loading & Cleaning

Removed irrelevant columns (id, Unnamed: 32)

Mapped diagnosis labels (M → 1, B → 0)

Split dataset into 70% training and 30% testing

Exploratory Data Analysis (EDA)

Visualized distributions of features by diagnosis type

Identified key indicators of malignancy (e.g., high radius, area, concavity)

Model Building & Evaluation
Implemented and tested multiple classification models:

Logistic Regression

Naive Bayes

Decision Tree

Random Forest
Evaluation metrics included:

Prediction accuracy on training and test sets

5-fold cross-validation scores

Key Findings
Random Forest consistently delivered the best performance.

Using the top 5 most important features (concave points_mean, area_mean, radius_mean, perimeter_mean, concavity_mean), the model achieved:

~95% accuracy on test data

~93% cross-validation score

Models using only one strong predictor (like radius_mean) still gave surprisingly high accuracy (~97%) but lower generalization.

Tools & Libraries Used
Python, Pandas, NumPy, Matplotlib for data manipulation and visualization

scikit-learn for model building, evaluation, and cross-validation

Models: LogisticRegression, GaussianNB, DecisionTreeClassifier, RandomForestClassifier

Conclusion
The Random Forest model with selected top features was the most accurate and reliable classifier in this analysis. Future work could include:

Hyperparameter tuning

Trying boosting models (e.g., XGBoost, LightGBM)

Automating feature selection and model comparison

