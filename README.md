# 💰 DSA210Project - Bank Transactions Analysis

**Spring 24-25 | DSA210 Term Project**

---

## 📝 Project Overview

This project analyzes my personal bank transaction history to uncover patterns in spending behavior, monitor cash flow trends, and identify recurring expenses or savings opportunities. By using exploratory data analysis, hypothesis testing, and derived feature creation, I aim to understand my financial habits more deeply and present meaningful insights.

---

## 🎯 Motivation

Managing personal finances efficiently is crucial for long-term financial well-being. This project serves as a practical tool for:

- Understanding monthly spending behavior
- Identifying major expense categories and irregularities
- Detecting recurring payments such as subscriptions or rent
- Monitoring income vs. expenses over time
- Laying the foundation for better financial planning and budgeting

---

## 🔎 Main Research Questions

### Spending & Income Patterns
- How do my expenses fluctuate across different months?
- What are my top spending categories?
- How much do I spend on recurring payments (subscriptions, rent, bills)?

### Cash Flow & Savings
- Am I consistently saving money, or spending more than I earn?
- How does my spending behavior change across the month?
- Are there notable spikes or anomalies in expense trends?

### Merchant & Transaction Analysis
- Which merchants or keywords appear most frequently?
- How often do I use digital payments vs. ATM withdrawals?
- Are there any duplicate or unexpected charges?

---

## 📊 Dataset Description

The dataset consists of personal bank transactions over a defined period. Each row includes:

- **Date & Time** – Transaction timestamp
- **Transaction Amount** – Positive for income, negative for expense
- **Account Balance** – Balance after the transaction
- **Description** – Merchant or transaction note
- **Transaction ID** – Unique transaction reference

---

## 🛠️ Feature Engineering

To make the analysis more informative, several features were created:
- **Month** and **Quarter** – for monthly/seasonal trend analysis
- **Day Type** – Weekday vs. Weekend indicator
- **Transaction Type** – Income vs. Expense
- **Rolling Averages** – 7-day and 30-day rolling averages for expense trends
- **Cumulative Balance** – Tracks peak savings over time
- **Transaction Label** – Tagged as "Transfer", "Rent", "Fee", etc., based on keywords in `Description`

This allowed the separation of routine/recurring expenses from discretionary spending.

---

## 📘 Key Findings from Statistical Testing

### 💸 Weekday vs. Weekend Spending
- A two-sample t-test was conducted to assess whether spending differs on weekends.
- **Result:** p = 0.1620 → Not statistically significant
- **Conclusion:** There is **no meaningful difference** between weekday and weekend spending in this dataset.

---

## 📅 Project Timeline

### ✅ March 10, 2025 – Project Proposal
- GitHub repository initialized
- Dataset and research questions defined

### 🔍 April 18, 2025 – Data Cleaning & EDA
- Skipped metadata rows and removed invalid entries
- Performed exploratory analysis on expenses, trends, and recurring patterns
- Conducted initial hypothesis testing

### 📑 May 30, 2025 – Final Submission
- Completed enriched analysis
- Added feature engineering and interpretations
- Prepared documentation, charts, and summary report



---

## 📂 Final Deliverables

- 📓 Jupyter Notebook with full analysis and comments
- 📈 Visualizations and charts to support findings
- 🧾 Cleaned dataset (non-sensitive)
- 📄 Final project report
- 🗃️ This GitHub repository containing all source files

---

## 🔧 Technologies Used

- Python (Pandas, Seaborn, Matplotlib, Scipy)
- Jupyter Notebook
- Google Colab
- Git & GitHub for version control

---

## 🚀 Future Work

- Integrate a budgeting model based on category spending
- Build an interactive dashboard using Streamlit or Dash
- Enrich dataset with external cost-of-living or inflation data
- Explore anomaly detection or transaction forecasting (optional ML)

---

_This repository will be updated if further improvements or extensions are added._
