📌 Project Overview

This project predicts whether a bank customer is likely to leave the bank. It uses the Churn Modelling dataset and a Machine Learning algorithm called Random Forest.

This project was completed as part of a college Machine Learning mini-project for Group 8.

🎯 Problem Statement

Can customer churn be predicted using customer demographic and banking information?

The goal is to train and evaluate a Random Forest classification model using the Churn Modelling dataset.

📊 Dataset

Dataset: Churn Modelling

Source: Kaggle

Target variable: Exited

Classes:

0 — Customer stayed

1 — Customer exited

The dataset contains customer and banking information. The code checks for the target column Exited and the categorical columns Geography and Gender.

🛠️ Technologies Used

Python

Pandas

NumPy

Matplotlib

Seaborn

Scikit-learn

Joblib

Google Colab

⚙️ Project Workflow

Data Loading and Inspection — checked the dataset size, column names, data types, sample records, missing values, and duplicate rows.

Data Cleaning — removed duplicate rows and records with a missing target value.

Exploratory Data Analysis (EDA) — plotted the target distribution and explored numerical features, age, geography, and gender.

Statistical Analysis — calculated range, quartiles, IQR, mean, mean absolute deviation, variance, standard deviation, and possible outliers.

Feature Preparation — removed identifier columns such as RowNumber, CustomerId, and Surname from the model features.

Data Preprocessing — filled missing numerical values with the median, filled missing categorical values with the most frequent value, and encoded categorical features using one-hot encoding.

Model Training — split the data into 80% training data and 20% testing data, then trained a Random Forest classifier.

Hyperparameter Tuning — used GridSearchCV with 3-fold stratified cross-validation to select model settings using F1 score.

Model Evaluation — measured accuracy, precision, recall, F1 score, and ROC-AUC.

Interpretation — generated charts and files to help understand the model's performance and important features.

🤖 Algorithm: Random Forest

Random Forest is a supervised Machine Learning algorithm that combines the predictions of multiple decision trees. It uses bootstrap sampling and random feature selection to build different trees and combines their results for a final prediction.

In this project, Random Forest is used to classify whether a customer stayed with the bank or exited.

📈 Evaluation Metrics

The model is evaluated using:

Accuracy

Precision

Recall

F1-score

ROC-AUC

Confusion Matrix

The project also creates a ROC curve, a learning curve, and a feature-importance chart. Actual scores are generated when the notebook is run; they are not written here because they depend on the run's output.

🧰 How to Run the Project

Option 1: Google Colab

1. Open the notebook in Google Colab.

2. Upload the dataset file named Churn_Modelling.csv.

3. Run the notebook cell.

4. Review the charts, metrics, and output files in the Group8_Project_Outputs folder.

Option 2: Run Locally

1. Download or clone your GitHub repository.

2. Keep Churn_Modelling.csv in the project folder.

3. Install the required libraries:

pip install pandas numpy matplotlib seaborn scikit-learn joblib

4. Save the notebook code as a Python file if you want to run it locally.

5. Run the Python file. If needed, provide the dataset path with --data and an output folder with --output.

📁 Main Output Files

The code creates a folder named Group8_Project_Outputs containing:

dataset_inspection.txt — dataset information and data checks

statistical_summary.csv — statistics and IQR outlier counts

outlier_summary.csv — outlier counts and percentages

pearson_correlation.csv — correlation values

metrics.json and classification_report.txt — evaluation results

07_confusion_matrix.png — confusion matrix

08_roc_curve.png — ROC curve

09_learning_curve.png — learning curve

feature_importance.csv and 10_feature_importance.png — feature importance

test_predictions.csv — actual and predicted churn labels and exit probabilities

random_forest_churn_model.joblib — saved trained model

The folder also contains EDA charts, including the target distribution, feature histograms, churn by geography and gender, correlation heatmap, and numerical boxplots.

🔍 Key Learning Outcomes

Understanding the main steps of a Machine Learning project.

Cleaning and exploring a dataset.

Using statistical measures and graphs to understand data.

Training a Random Forest classification model.

Using cross-validation and hyperparameter tuning.

Evaluating classification results using several metrics.

Understanding feature importance and model limitations.

⚠️ Disclaimer

This project is for educational purposes. Predictions are based on the supplied dataset and may not apply to every bank or customer group. Feature importance does not prove that a feature causes a customer to leave.

👨‍💻 Project Information

Group: 8

Project: Customer Churn Prediction

Algorithm: Bagging – Random Forest

Dataset: Churn Modelling
