# Heart_disease_prediction-
HEART DISEASE_PNG.jpg

## Exploratory Data Analysis Report
## 1. Dataset Overview
Shape: The dataset consists of 303 rows and 14 columns.
Features: It contains both numerical and categorical variables. The target variable is target, which indicates the presence (1) or absence (0) of heart disease.
No Missing Values: All columns have complete data, meaning no imputation is required.
Data Types:
Numerical: age, trestbps (resting blood pressure), chol (serum cholesterol), thalach (maximum heart rate), oldpeak.
Categorical: sex, cp (chest pain type), fbs (fasting blood sugar), restecg (resting ECG results), exang (exercise-induced angina), slope, ca (number of major vessels), thal, target.
## 2. Summary Statistics
Numerical Features
Age:
Ranges from 29 to 77 years, with a mean of approximately 54 years.
The distribution is slightly right-skewed, with most individuals clustered between 40 and 60.
Resting Blood Pressure (trestbps):
Mean: 131 mmHg, with values ranging from 94 to 200 mmHg.
Nearly normal distribution, but with slight outliers at higher values.
Cholesterol (chol):
Mean: 246 mg/dL, ranging from 126 to 564 mg/dL.
Skewed to the right, indicating instances with high cholesterol.
Maximum Heart Rate (thalach):
Mean: 149 bpm, ranging from 71 to 202 bpm.
Positively correlated with the presence of heart disease.
Oldpeak:
Mean: 1.04, indicating ST depression relative to rest.
Right-skewed, with most values below 2.
Categorical Features
Sex: 68% male (1) and 32% female (0).
Chest Pain Type (cp):
Type 0 (typical angina) is the least frequent.
Types 1, 2, and 3 are fairly balanced.
Fasting Blood Sugar (fbs):
Majority (85%) have fasting blood sugar ≤ 120 mg/dL.
Exercise-Induced Angina (exang):
67% reported no angina during exercise.
## 3. Key Observations from Visualizations
Numerical Distributions
Most features (e.g., age, chol, thalach) show normal or slightly skewed distributions.
chol and oldpeak have noticeable outliers, which may affect the model's performance.
Correlation Heatmap
Strong Positive Correlation: thalach (maximum heart rate) is inversely correlated with heart disease. Higher heart rates are associated with a lower likelihood of disease.
Weak Correlations: Other variables like chol and trestbps show weak or no correlation with the target.
Categorical Features
Sex: Males have a higher prevalence of heart disease.
Chest Pain Type (cp):
Non-anginal pain (type 2) and asymptomatic cases (type 3) are strongly associated with heart disease.
Number of Vessels Colored (ca):
Higher values (3 or 4) correlate with a higher likelihood of disease.
Slope: Patients with a flat slope (2) are more likely to have heart disease.
Pairplot Insights:
The pairplot highlights relationships between numerical features (age, thalach, chol, etc.) and the target:
Individuals with higher thalach values tend to have lower heart disease prevalence.
oldpeak values are generally higher for those with heart disease.
## 4. Actionable Insights for Modeling
Feature Selection:
Features such as thalach, cp, slope, and ca show strong or moderate associations with the target variable and should be prioritized during feature selection.
Features like trestbps and chol have weak correlations but may still contribute in combination with other features.
Outlier Treatment:
Address outliers in chol, trestbps, and oldpeak using techniques like clipping or scaling to improve model robustness.
Scaling:
Normalize numerical features (age, trestbps, chol, thalach, oldpeak) to standardize ranges and improve algorithm performance.
Feature Engineering:
Create interaction terms or bin features like age into age groups.
Explore one-hot encoding for categorical variables (cp, thal, slope) for machine learning models.
## 5. MODEL TRAINING
Performed data preprocessing to handle outliers and scale features.
Use feature importance techniques (e.g., correlation analysis or tree-based models) to finalize feature selection.
Split the data into training and testing sets and proceed with model training using algorithms like Logistic Regression, Random Forest, or Gradient Boosting.
