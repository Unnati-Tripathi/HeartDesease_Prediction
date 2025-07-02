# HeartDesease_Prediction

Objective:
To build a machine learning model that predicts whether a patient has heart disease (target = 1) or not (target = 0), based on their medical attributes.

# **🔍 Step-by-Step Workflow:**

# **1. Data Loading & Understanding**
Loaded data using Pandas.

Used data.info(), data.describe() and isnull() to understand structure, data types, and confirm no missing values.

# **2. Data Visualization & Exploration**
Used:

Pairplots (sns.pairplot) to visualize distributions.

Countplots for categorical features vs target.

Strip plots / scatter plots for numeric feature trends vs target.

Correlation heatmap to understand linear relationships.

# **3. Preprocessing**
Encoded categorical variables using pd.get_dummies() with drop_first=True to avoid multicollinearity.

Normalized numeric data using StandardScaler() to make features comparable for ML algorithms.

# **4. Train-Test Split**
Split data into 80% training and 20% testing using train_test_split(stratify=y) to maintain label distribution.

# **5. Model Training & Evaluation**
🔹 Logistic Regression (Base Model)
Accuracy: ~87%

Interpretable and efficient on normalized data.

🔹 Recursive Feature Elimination (RFE)
Used RFE to select the top 10 important features, but accuracy slightly dropped.

🔹 Random Forest Classifier (Best Model)
Accuracy: ~90%

Robust to outliers and irrelevant features.

Confusion matrix and classification report showed high precision and recall for both classes.

# **✅ Final Outcome:**
Random Forest outperformed logistic regression in accuracy and F1-score.

The model can reliably predict heart disease from patient records.

Important features include: cp, thal, oldpeak, thalach, exang.



Try advanced models like XGBoost or SVM.

Deploy as a simple web app using Flask or Streamlit.

