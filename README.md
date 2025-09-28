🏦 Bank Marketing Campaign Prediction using Decision Trees 🎯
📌 Project Overview

This project focuses on predicting whether a customer will subscribe to a bank term deposit based on their demographic and campaign interaction details. The goal is to build and optimize a Decision Tree Classifier using data preprocessing, categorical encoding, model training, and hyperparameter tuning.

📂 Workflow Summary
✅ 1. Importing Libraries

The project uses:

Pandas for data handling

Matplotlib for visualization

Scikit-learn for encoding, modeling, evaluation, and tuning

📁 2. Loading the Dataset

The dataset (Bank.csv) is read using semicolon (;) as a separator. Initial inspection is done to understand structure and column types.

🛠 3. Data Wrangling with Custom Function

A reusable function named wrangle() is defined to:

✔ Convert "yes"/"no" values in columns like y, default, housing, loan into Boolean True/False

✔ Categorize customer balances into 5 balance groups using a custom function balanceator():

Class E: Very Low Balance (<72)

Class D: Low Balance (72–447)

Class C: Medium Balance (448–1427)

Class B: High Balance (up to 99th percentile)

Class A: Top 1% Elite Customers

✔ Create previous_bool — a derived flag indicating whether a customer was contacted before

✔ Drop unnecessary columns:
previous, day, poutcome, pdays

✂️ 4. Feature & Target Selection

Target (y) → Whether the client subscribed (True / False)

Features (X) → All other columns except balance and duration which were removed as irrelevant or risky for leakage

🔢 5. Encoding Categorical Variables

All non-numeric columns are converted to numerical format using Ordinal Encoding.

🔄 6. Train-Test Split

The dataset is split into:

Training Set → 85%

Testing Set → 15%

Using stratification to preserve class balance.

🌳 7. Initial Model — Baseline Decision Tree

A GridSearchCV is applied initially without parameters, optimized for recall to reduce False Negatives (important in marketing predictions).

Model performance is visualized using a Confusion Matrix, followed by a Classification Report.

🔧 8. Hyperparameter Tuning

A refined GridSearchCV is run using the following search space:

Hyperparameter	Values Tested
max_depth	5, 10, 15, 20, 25, 30, None
criterion	gini, entropy
min_samples_split	2, 3
min_samples_leaf	1, 2
🏦 Bank Marketing Campaign Prediction using Decision Trees 🎯
📌 Project Overview

This project focuses on predicting whether a customer will subscribe to a bank term deposit based on their demographic and campaign interaction details. The goal is to build and optimize a Decision Tree Classifier using data preprocessing, categorical encoding, model training, and hyperparameter tuning.

📂 Workflow Summary
✅ 1. Importing Libraries

The project uses:

Pandas for data handling

Matplotlib for visualization

Scikit-learn for encoding, modeling, evaluation, and tuning

📁 2. Loading the Dataset

The dataset (Bank.csv) is read using semicolon (;) as a separator. Initial inspection is done to understand structure and column types.

🛠 3. Data Wrangling with Custom Function

A reusable function named wrangle() is defined to:

✔ Convert "yes"/"no" values in columns like y, default, housing, loan into Boolean True/False

✔ Categorize customer balances into 5 balance groups using a custom function balanceator():

Class E: Very Low Balance (<72)

Class D: Low Balance (72–447)

Class C: Medium Balance (448–1427)

Class B: High Balance (up to 99th percentile)

Class A: Top 1% Elite Customers

✔ Create previous_bool — a derived flag indicating whether a customer was contacted before

✔ Drop unnecessary columns:
previous, day, poutcome, pdays

✂️ 4. Feature & Target Selection

Target (y) → Whether the client subscribed (True / False)

Features (X) → All other columns except balance and duration which were removed as irrelevant or risky for leakage

🔢 5. Encoding Categorical Variables

All non-numeric columns are converted to numerical format using Ordinal Encoding.

🔄 6. Train-Test Split

The dataset is split into:

Training Set → 85%

Testing Set → 15%

Using stratification to preserve class balance.

🌳 7. Initial Model — Baseline Decision Tree

A GridSearchCV is applied initially without parameters, optimized for recall to reduce False Negatives (important in marketing predictions).

Model performance is visualized using a Confusion Matrix, followed by a Classification Report.

🔧 8. Hyperparameter Tuning

A refined GridSearchCV is run using the following search space:

Hyperparameter	Values Tested
max_depth	5, 10, 15, 20, 25, 30, None
criterion	gini, entropy
min_samples_split	2, 3
min_samples_leaf	1, 2
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/0518710a-a5eb-46b4-b486-d69ecd98ef31" />

