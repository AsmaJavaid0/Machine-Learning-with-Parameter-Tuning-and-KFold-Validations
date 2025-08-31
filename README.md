🧠 ##Machine Learning Regression Pipeline with Cross-Validation & Hyperparameter Tuning
📌 Project Overview

This project demonstrates a complete end-to-end machine learning pipeline for solving a regression problem. It covers everything from data preprocessing, feature engineering, scaling & encoding, cross-validation, hyperparameter tuning, and model evaluation to visualization of predictions vs actual values.

The pipeline ensures that the trained model is robust, reliable, and generalizable by using advanced evaluation techniques.

⚙️ ## Workflow

Data Loading – Import dataset and prepare features (X) and target (y).

Data Preprocessing – Handle categorical and numerical features using encoding and scaling.

Feature Engineering – Extract time-based features like Year, Month, Day, Hours, and Minutes.

Scaling & Encoding –

OrdinalEncoder for categorical variables (City, Customer type, Gender, Product line, Season)

StandardScaler for numerical variables (Unit price, Quantity, Tax 5%, Total, COGS, Year, Month, Day, Hours, Minutes)

KFold Cross-Validation – Perform 5-fold CV to evaluate model consistency.

Training & Hyperparameter Tuning –

Base model: LinearRegression

Hyperparameter optimization using RandomizedSearchCV

Prediction & Testing – Test on unseen data to check model generalization.

Visualization – Plot predictions vs actual values for better interpretation.

📊 Evaluation Metrics

During Cross-Validation and final testing, the following metrics are calculated:

MAE (Mean Absolute Error)

MSE (Mean Squared Error)

RMSE (Root Mean Squared Error)

R² (Coefficient of Determination)

Example output (your results may differ):

Cross-Validation Results (Regression):
MAE: 4.231 ± 0.482
MSE: 28.545 ± 3.112
RMSE: 5.345 ± 0.321
R²: 0.892 ± 0.025

🔎 Hyperparameter Tuning

Grid searched parameters for Linear Regression:

fit_intercept: [True, False]

copy_X: [True, False]

n_jobs: [None, 1, 2, 3, -1]

positive: [True, False]

Example best parameters found:

{
  "fit_intercept": true,
  "copy_X": true,
  "n_jobs": -1,
  "positive": false
}

📈 Visualization

The scatter plot below compares predicted vs actual values.

Blue points → Predictions

Red dashed line → Ideal (perfect prediction line)

This helps in visually inspecting model performance.

🛠 Tech Stack

Python 3.9+

Libraries:

pandas, numpy, matplotlib

scikit-learn (for preprocessing, modeling, CV, and metrics)

