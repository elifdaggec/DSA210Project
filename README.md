# 💰 DSA210Project - Bank Transactions Analysis

**Spring 24-25 | DSA210 Term Project**

---

## 📝 Project Overview

This project analyzes my personal bank transaction history to uncover patterns in spending behavior, monitor cash flow trends, identify recurring expenses, and support personal financial planning. By applying data science and machine learning techniques, the project generates actionable insights and behavioral patterns from raw transaction records.

---

## 🎯 Motivation

Managing personal finances efficiently is crucial for long-term well-being. This project helps:

- Understand personal spending behavior and identify high-cost categories
- Detect recurring payments such as subscriptions, rent, and fees
- Monitor cash flow and saving trends across months
- Identify unusual or outlier transactions
- Form the basis for automated financial tracking or budgeting tools

---

## 🔎 Main Research Questions

### Spending & Income Patterns
- How do my expenses vary month to month?
- What are my top spending categories?
- How much do I spend on subscriptions, rent, or transfer-like recurring transactions?

### Cash Flow & Savings
- Am I saving more than I spend each month?
- Do I spend more on weekends or weekdays?
- Are there specific dates with spikes or anomalies in expense amounts?

### Merchant & Transaction Analysis
- Which merchants or transaction types appear most often?
- What’s the distribution between card use, cash withdrawal, and transfers?
- Are there any duplicate or suspicious transactions?

---

## 📊 Dataset Description

The dataset consists of transaction-level data exported from a personal banking portal.

| Feature             | Description                                        |
|---------------------|----------------------------------------------------|
| `Date & Time`       | When the transaction occurred                      |
| `Transaction Amount`| Amount in TL (positive = income, negative = expense) |
| `Account Balance`   | Account balance after the transaction              |
| `Description`       | Text info like merchant, source, or reference      |
| `Transaction ID`    | Unique transaction identifier                      |

---

## 🛠️ Feature Engineering

Several new features were created to enrich the dataset for analysis and modeling:

- `Month` and `Quarter` – to detect seasonal patterns
- `Day Type` – Weekday vs Weekend indicator
- `Transaction Type` – Income or Expense
- `Rolling Averages` – 7-day and 30-day spending trends
- `Cumulative Balance` – to track financial progress over time
- `Transaction Label` – Tagged as "Transfer", "Rent", "Fee", etc. using keyword rules

---

## 📘 Key Statistical Finding

### 💸 Weekday vs. Weekend Spending

- A two-sample t-test was conducted.
- **p-value = 0.1620** → No significant difference
- **Interpretation:** Spending is consistent across weekdays and weekends.

---

## 🧠 Machine Learning Applications

### ✅ 1. Supervised Classification – Predict Transaction Type

We trained two models to classify whether a transaction is an **Income (1)** or **Expense (0)** based on amount, time, and labels.

**Features Used:**
- Transaction Amount
- Month and Quarter
- Day Type
- Rolling Averages
- Transaction Label

**Results:**

| Model               | Accuracy |
|---------------------|----------|
| Logistic Regression | 99.47%   |
| Random Forest       | 99.47%   |

✅ Both models performed exceptionally well, showing the task is highly learnable.

---

### ✅ 2. Unsupervised Clustering – Discover Transaction Groups

We applied **K-Means clustering (k=5)** to uncover behavioral spending patterns.

**Input Features:**
- Amount
- Month
- Rolling Averages
- Day Type & Transaction Label (encoded)

**Cluster Insights:**
- One cluster includes mostly **rent payments**
- Another groups **salary/income entries**
- Others represent **daily or discretionary spending**
- Outlier cluster with a single high-value transaction

Visualizations:
- 📊 Cluster sizes (bar plot)
- 📈 Transaction amount vs. month (scatter plot)
- 💸 Boxplot of transaction distributions per cluster

These clusters help segment financial behaviors for budgeting or anomaly detection.

---

## 📂 Final Deliverables

- 📓 Cleaned and annotated Jupyter Notebook
- 📈 Visualizations and charts for trends and clusters
- 🔢 Feature-enriched dataset
- 📄 Statistical analysis and hypothesis testing
- 🧠 ML models with performance summaries
- 🗂️ This GitHub repository

---

## 🔧 Technologies Used

- Python: `pandas`, `scikit-learn`, `seaborn`, `matplotlib`
- Jupyter Notebook / Google Colab
- GitHub for version control and documentation

---

## 🚀 Future Work

- Add predictive budgeting tools
- Visualize monthly summaries as a dashboard
- Detect anomalies or suspicious entries automatically
- Extend analysis across multiple accounts or institutions

---

_This repository will continue to be updated as part of ongoing financial self-tracking and experimentation._
