# 📊 Intuit QuickBooks Upgrade – Response Modeling  

This project applies **predictive modeling and campaign optimization** to the **Intuit QuickBooks Upgrade case study**. The challenge: identify which customers are most likely to respond to a **second-wave mailing** for QuickBooks Version 3.0, in order to **maximize profit while minimizing wasted marketing spend**.  

---

## 📌 Project Overview  
In 1995, Intuit launched a direct mail campaign to over 800,000 customers, offering an upgrade to QuickBooks 3.0. The **first wave mailing** generated nearly 40,000 purchases, but the marketing team faced a key decision:  

👉 Should the **second wave mailing** be sent to *all non-responders*, or should it be **selectively targeted** to maximize profitability?  

This project leverages **customer-level historical data** to build predictive models that estimate response probabilities and guide **optimal mailing decisions**.  

**Objectives:**  
1. Predict customer likelihood to respond to the upgrade offer.  
2. Compare alternative models (Logistic Regression, Neural Networks, XGBoost).  
3. Simulate second-wave targeting strategies.  
4. Quantify expected **profit lift** from selective targeting.  
5. Provide insights into characteristics of businesses most likely to upgrade.  

---

## 🔍 Methodology  

### 1. Data Preparation  
- **Dataset:** 75,000 small businesses (subset of the original 801,821 mailed in wave-1).  
- **Key Variables:**  
  - Customer demographics (zip code bins, gender, business flag).  
  - Historical purchase behavior (orders, revenue, recency, original purchase).  
  - Product characteristics (current version, tax product ownership, prior upgrades).  
  - Response flag for wave-1 (`res1`).  
- **Splits:** 70% training, 30% test (22,500 in test set).  

---

### 2. Modeling Approach  
- **Baseline Model:** Logistic Regression (interpretable benchmark).  
- **Advanced Models:**  
  - Neural Networks (capture non-linear patterns).  
  - XGBoost (boosted trees with hyperparameter tuning).  
- **Evaluation Metrics:** AUC, Lift Curves, Gains Charts, and **Expected Profit**.  
- **Adjustment:** Wave-2 response assumed to be **50% of wave-1 predicted probability** (industry standard).  

---

### 3. Profit Simulation  
- **Mailing Cost:** $1.41 per customer.  
- **Revenue Margin:** $60 per responder (excluding mailing cost).  
- **Scenarios compared:**  
  1. **Mail All Non-Responders** (status quo).  
  2. **Mail None** (conservative).  
  3. **Selective Targeting with Predictive Models** (optimized).  

Results show that **model-driven targeting significantly increases profitability**, avoiding wasted spend on low-probability customers.  

---

## 🛠️ Tools & Libraries  
- **Python:** pandas, numpy, matplotlib, seaborn  
- **scikit-learn:** logistic regression, neural networks, evaluation metrics  
- **XGBoost:** advanced boosting for predictive accuracy  
- **pyrsm package:** profit, lift, and gains analysis utilities  
- **Jupyter Notebook:** fully reproducible workflow  

---

## 💡 Key Skills & Concepts  
- **Response Modeling for Direct Marketing**  
- **Customer Targeting & Segmentation**  
- **Profit-Based Evaluation (beyond accuracy)**  
- **Model Comparison (Logistic, Neural Nets, XGBoost)**  
- **Campaign Optimization & Simulation**  
- **Business Analytics for Marketing ROI**  

---

## 🚀 Key Takeaways  
- **Not all customers should be mailed** — targeting only high-probability responders maximizes ROI.  
- **Model-driven targeting** produces higher profit compared to mailing everyone.  
- **Zip code, recency of purchase, and prior upgrades** were key predictors of response.  
- The case demonstrates how **analytics transforms marketing efficiency** and reduces unnecessary spend.  

---
