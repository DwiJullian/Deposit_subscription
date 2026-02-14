# 📊 Term Deposit Subscription Prediction

This project was developed as part of a data science competition. The goal is to build a machine learning model that predicts whether a bank customer will subscribe to a **term deposit product**.

---

# 🏦 Business Context

In the banking industry, marketing campaign effectiveness plays a crucial role in profitability. Banks frequently conduct telemarketing or outreach campaigns to offer financial products such as term deposits.

However, several challenges arise:

* Not all customers are interested in subscribing
* Contacting customers incurs operational costs (telemarketing, SMS, email campaigns)
* Response rates are typically low (the dataset is imbalanced)

By leveraging historical data such as:

* Customer demographics
* Loan history
* Previous campaign outcomes
* Macroeconomic indicators

Banks can develop predictive models to improve campaign efficiency.

---

# ❗ Business Problem

Without a predictive model:

* Banks contact many customers who are not interested
* Operational costs increase
* Conversion rates remain low
* Marketing teams do not work optimally

The core problem:

> How can we identify customers who are most likely to subscribe to a term deposit in order to make marketing campaigns more effective and efficient?

---

# 🎯 Business Objective

To build a classification model that predicts:

* **1** → Customer is predicted to subscribe to a term deposit
* **0** → Customer is predicted not to subscribe

The ultimate objectives are:

* Increase campaign conversion rate
* Reduce marketing costs
* Optimize sales team resource allocation
* Increase bank revenue from term deposit products

---

# 📈 Business Metrics

Since the dataset is **imbalanced** (the number of customers subscribing is significantly lower than those who do not), business evaluation focuses on:

### 1️⃣ Precision (Positive Class)

Measures how many customers predicted as subscribers actually subscribe.

👉 Important to avoid wasting marketing resources.

---

### 2️⃣ Recall (Positive Class)

Measures how many actual potential subscribers are correctly identified.

👉 Important to avoid missing high-potential customers.

---

### 3️⃣ Conversion Rate Improvement

Compare campaign conversion rate before and after implementing the model.

---

### 4️⃣ Cost Efficiency

Measure the reduction in unnecessary customer contacts.

---

# 🤖 Machine Learning Approach

## Target Variable

`berlangganan_deposito`

* 1 → Subscribed
* 0 → Not subscribed

## Feature Selection

Features include:

* Demographic attributes (age, education, marital status)
* Credit history (previous default, loans)
* Previous campaign history
* Macroeconomic indicators

---

# 📊 ML Metrics

Initially, hyperparameter tuning was performed using **ROC-AUC**.

However, due to class imbalance, ROC-AUC was not the most appropriate metric.

---

## ❌ Limitation of ROC-AUC in Imbalanced Data

ROC-AUC can appear high even when the model performs poorly on the minority class.

---

## ✅ More Appropriate Metric: PR-AUC

**Precision-Recall AUC (PR-AUC)** is more suitable because:

* It focuses on performance for the positive class (subscribers)
* It is more sensitive to errors in minority class prediction
* It aligns better with business objectives

---

# 🔧 Modeling Strategy

* Data preprocessing
* Categorical encoding
* Hyperparameter tuning
* Model evaluation using:

  * PR-AUC (primary metric)
  * Precision
  * Recall
  * F1-Score

---

# 📌 Insights & Lessons Learned

The main mistake in this project:

> Using ROC-AUC as the primary tuning metric on an imbalanced dataset.

---

# 🚀 Expected Business Impact

With this model, the bank can:

* Reduce random or inefficient customer outreach
* Improve campaign efficiency
* Increase closing probability
* Optimize marketing operational costs

---

# 🧠 Conclusion

This project highlights that:

* Machine learning is not just about achieving high accuracy
* Metric selection must align with both data characteristics and business objectives
* In imbalanced classification problems, PR-AUC is more informative than ROC-AUC
