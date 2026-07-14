# Credit Card Fraud Risk Analysis

This project explores credit card fraud using Python, SQL, machine learning, and Power BI. The goal was to understand what makes fraudulent transactions different from legitimate ones, identify meaningful patterns in the data, and build a simple model that can predict whether a transaction is likely to be fraudulent.

The project follows a complete analytics workflow, from cleaning raw data to building a dashboard and training a machine learning model.

---

## Dataset

- 100,000 credit card transactions
- 31 original features
- Target variable: `is_fraud`

Fraud made up only **0.6%** of the dataset (598 out of 100,000 transactions), making it a highly imbalanced classification problem.

---

## What I Did

### Data Exploration

I started by exploring the dataset to understand its structure, identify missing values, and examine the distribution of fraudulent transactions.

### Data Cleaning & Feature Engineering

To make the data more useful for analysis, I:

- Converted transaction timestamps into datetime format
- Created new features such as:
  - Hour of day
  - Day of week
  - Month
- Checked for missing values and cleaned relevant columns

### SQL Analysis

Using SQLite, I answered a few business-focused questions:

- Which payment method has the highest fraud rate?
- Does transaction type affect fraud?
- What time of day has the highest fraud rate?
- How do fraud transaction amounts compare to legitimate ones?

### Exploratory Data Analysis

I visualized the data to better understand fraud patterns, including:

- Fraud rate by hour of day
- Fraud rate by payment method
- Distribution of transaction amounts

### Machine Learning

I built a Logistic Regression model using:

- Transaction amount
- Hour of day
- Payment method
- Transaction type

To deal with the severe class imbalance, I used:

- One-hot encoding
- Stratified train-test split
- `class_weight='balanced'`

---

## Key Findings

- Fraud represented only **0.60%** of all transactions.
- Fraud rates increased significantly between **10 PM and 11 PM**, reaching roughly **3%**, almost **5× higher** than the overall fraud rate.
- Fraudulent transactions had an average value of **541.56**, compared to **67.26** for legitimate transactions.
- Credit cards showed a slightly higher fraud rate than debit cards and mobile payments, although the difference was relatively small.

---

## Model Performance

**Model:** Logistic Regression

| Metric | Score |
|---------|------:|
| Accuracy | **95.06%** |
| Recall (Fraud) | **82%** |
| Precision (Fraud) | **9%** |

The model successfully identified most fraudulent transactions, but also flagged a large number of legitimate transactions. This highlights the tradeoff between detecting fraud and reducing false positives when working with highly imbalanced datasets.

---

## Dashboard

The Power BI dashboard summarizes the key findings and includes:

- Total Transactions
- Fraud Cases
- Fraud Rate
- Average Fraud Amount
- Fraud Rate by Hour of Day
- Fraud Rate by Payment Method
- Fraud Rate by Transaction Type

## What I'd Improve Next

If I continued working on this project, I would:

- Try tree-based models like Random Forest or XGBoost
- Engineer additional time-based features
- Include more customer and merchant information
- Tune the classification threshold to improve the balance between precision and recall

---

## Tools Used

- Python
- Pandas
- SQL (SQLite)
- Matplotlib
- Scikit-learn
- Power BI

---

## Author

**Adithya K P**


<img width="798" height="522" alt="image" src="https://github.com/user-attachments/assets/5f6f0269-e81f-4841-9595-42a27d83977f" />
<img width="1175" height="634" alt="image" src="https://github.com/user-attachments/assets/63998fce-ef4a-4011-bac8-1746abd3f3f6" />
<img width="841" height="586" alt="image" src="https://github.com/user-attachments/assets/692b2f69-0dff-4ae4-8704-b6b0846586c6" />
