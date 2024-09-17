# TelecomClassification

Objective:

To create a model to predict the likelihood (percentile) of customer churn in the future.

1. Initial Data Exploration:

Data Cleaning:

Dropped irrelevant columns such as CustomerID, Count, Zip Code, Lat Long, etc.
Addressed missing values (NaNs) in columns.
"Churn Reason" column had excessive NaNs and unique values, which were deemed irrelevant for the analysis.
Exploratory Data Analysis (EDA):

Performed data visualization on numerical and categorical features.
Analyzed the correlation matrix to understand relationships between features and the target variable.
2. Data Preparation:

Feature Classification:

Grouped numerical features into float and int types.
Grouped categorical features into object types.
Data Imputation and Encoding:

Imputed missing values.
Encoded categorical variables.
Combined numerical and categorical data into a single dataset.
Feature Engineering:

Created interaction features to enhance the model’s predictive capability.
3. Target Variable:

Identification:

Defined Churn Value as the target variable (y_variable).
Analyzed the distribution of the target variable, finding a class imbalance with 2000 churn (1) vs. 6000 no churn (0).
Class Balancing:

Applied Synthetic Minority Over-sampling Technique (SMOTE) to address class imbalance and balance the dataset.
4. Model Selection and Evaluation:

Models Tested:

K-Nearest Neighbors (KNN)
Decision Tree
Random Forest
Cross-Validation Techniques Used:

Grid Search for hyperparameter tuning.
Stratified K-Fold Cross-Validation for model validation.
Cross-validation scores were used to assess model performance.
Performance Metrics:

Evaluated models based on accuracy, mean accuracy, and standard deviation.
Random Forest showed a 1.00 accuracy, which was identified as overfitting.
Decision Tree provided an 83% accuracy, which was selected as the final model due to its more generalizable performance.
5. Final Model:

Decision Tree: Chosen as the final model based on its balance between accuracy and overfitting, providing a more robust prediction compared to the Random Forest model.
