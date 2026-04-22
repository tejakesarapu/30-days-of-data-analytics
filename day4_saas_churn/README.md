# 📊 Day 4 — Exploratory Data Analysis (EDA) on SaaS Churn Dataset


## 🚀 Overview

Day 4 focuses on **Exploratory Data Analysis (EDA)** — the stage where raw data is transformed into **meaningful insights**.

Unlike data cleaning (Day 3), EDA is about:

* Understanding patterns
* Discovering relationships
* Identifying key business drivers

This project analyzes a **multi-table SaaS dataset** to uncover **churn behavior, customer engagement, and revenue trends**.

---

## 🗂️ Dataset Structure (Relational SaaS Model)

This project uses multiple datasets representing a real-world SaaS system:

```
📁 data/
│
├── ravenstack_accounts.csv          → Customer details
├── ravenstack_subscriptions.csv     → Subscription & billing info
├── ravenstack_feature_usage.csv     → Product usage logs
├── ravenstack_support_tickets.csv   → Customer support interactions
├── ravenstack_churn_events_cleaned.csv → Churn information
```

---

## 🧠 Data Modeling Approach

All datasets were merged into a **single analytical dataset** using:

* `account_id` → Primary key
* `subscription_id` → Usage mapping

### 🔗 Final Dataset Features:

| Category      | Features                             |
| ------------- | ------------------------------------ |
| Customer Info | industry, country, referral_source   |
| Revenue       | mrr_amount, arr_amount               |
| Usage         | usage_count, usage_duration_secs     |
| Support       | total_tickets, resolution_time_hours |
| Behavior      | satisfaction_score, escalation_flag  |
| Derived       | tenure_days, seat_utilization        |
| Target        | churned                              |

---

## 🛠️ Feature Engineering

Key engineered features:

* **tenure_days** → Customer lifetime
* **seat_utilization** → subscription_seats / account_seats
* **churned** → Target variable

---

## 📊 EDA Process

### 🔹 1. Descriptive Analysis

* Statistical summary using `.describe()`
* Group comparison: churn vs non-churn

---

### 🔹 2. Univariate Analysis

* Distribution of revenue, usage, tenure
* Identification of skewness and outliers

---

### 🔹 3. Bivariate Analysis

* Relationship between features and churn:

  * Usage vs Churn
  * Tenure vs Churn
  * Tickets vs Churn
  * Plan Tier vs Churn

---

### 🔹 4. Multivariate Analysis

* Combined impact of:

  * Usage + Support → Churn
  * Tenure + Revenue → Retention
  * Seat Utilization → Product Adoption

---

### 🔹 5. Correlation Analysis

* Heatmap to identify strong relationships
* Focus on variables influencing churn

---

### 🔹 6. A/B Testing (Statistical Validation)

Performed hypothesis testing using **t-tests**:

* Trial vs Non-Trial Users
* High Usage vs Low Usage
* Plan Tier comparisons

---

## 🔥 Key Insights

### 📉 1. Low Usage Drives Churn

Customers with low product usage are significantly more likely to churn.

---

### ⏳ 2. Early Lifecycle Risk

Customers with low tenure show higher churn → onboarding is critical.

---

### 💰 3. Revenue vs Retention

Higher MRR customers are more stable and less likely to churn.

---

### 🧪 4. Trial Users Churn More

A/B testing confirms that trial users have higher churn rates.

---

### 📦 5. Seat Utilization Matters

Underutilized accounts are more likely to churn → poor adoption signal.

---

### 🎫 6. High Support Dependency = Risk

Customers raising more support tickets (with low usage) tend to churn.

---

### ⭐ 7. Satisfaction Impacts Retention

Lower satisfaction correlates with higher churn (secondary driver).

---

## 🧠 Business Conclusion

> Churn is primarily driven by **low engagement, poor onboarding, and underutilization of the product**.

---

## 💡 Recommendations

* Improve onboarding experience
* Increase product engagement tracking
* Optimize trial conversion strategy
* Monitor seat utilization
* Reduce product friction via support insights

---

## 🧰 Tech Stack

* Python 🐍
* Pandas
* NumPy
* Seaborn & Matplotlib
* SciPy (A/B Testing)

---

## 📁 Project Structure

```
📁 Day-4-EDA-SaaS-Churn/
│
├── data/
├── notebooks/
│   ├── eda.ipynb
│   └── data_cleaning.ipynb
│
├── README.md
```

---

## 🎯 Outcome

This project demonstrates:

* Real-world data modeling
* End-to-end EDA workflow
* Business-driven insights
* Statistical validation

---

## 🔗 Dataset Source

Kaggle SaaS Churn Dataset
https://www.kaggle.com/datasets/rivalytics/saas-subscription-and-churn-analytics-dataset

---

## 🙌 Final Note

This is not just EDA — this is **business problem solving using data**.

---


