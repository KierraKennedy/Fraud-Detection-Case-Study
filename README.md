# Subscription Fraud Detection Case Study

## 🚀 Overview

Built a fraud detection analysis for a subscription-based product using device, behavioral, and payment signals.

Identified high-risk user patterns, developed a rule-based risk scoring system, and estimated revenue exposure from fraudulent activity.

👉 Focus: fraud prevention, risk segmentation, and revenue protection

---

## ⚡ Key Results (30-Second Read)

- Identified ~15% of users as high-risk based on behavioral and payment signals  
- Fraud is concentrated among:
  - multi-account device usage (device farms)
  - high refund frequency
  - VPN / cloud-based traffic  
- Chargebacks show near-100% fraud rates, acting as a strong downstream signal  

💰 Estimated revenue exposure: **~$4,500/month**

👉 Built a rule-based risk scoring system that segments users into low, medium, and high-risk tiers, enabling faster detection and reduced manual review effort


## ▶️ Open the Project

📊 **Main Analysis Notebook:**  
  `Fraud_Case_Study.ipynb`

🧪 **Dataset Generator:**  
  `Fraud_Risk.ipynb`

## 📊 Key Analyses

### 1. Risk Segmentation (Review Buckets)
- High risk users show near total fraud concentration
- Low risk users have minimal fraud rates
- Confirms the effectiveness of the risk scoring system

### 2. Device Reuse Analysis
- Fraud increases sharply as accounts per device increase
- Strong indicator of device farming / coordinated abuse

### 3. Refund Behavior
- Users with multiple refunds are significantly more likely to be fraudulent
- Refund frequency is a high-signal feature for detection systems

### 4. Payment Outcome (Fraud Funnel)
- Chargebacks and refunds have the highest fraud rates
- Paid transactions show the lowest fraud likelihood
- Payment outcomes act as downstream fraud signals

### 5. Financial Impact
- Fraud directly impacts revenue
- Even small fraud rates scale into meaningful financial losses






## 🧠 Key Insights

1. Fraud rates increase significantly when multiple accounts share the same device  
2. Refund heavy users are much more likely to be fraudulent  
3. Fraud is more concentrated on cloud and VPN networks than residential networks  
4. New accounts show elevated fraud risk  
5. Risk scoring effectively concentrates fraud into higher risk buckets  
6. Chargebacks and refund outcomes are strongly associated with fraud  


## 🏢 Business Recommendations

1. Limit account creation from heavily reused devices  
2. Flag users with 2 + refunds within 90 days for manual review  
3. Apply higher risk scores to VPN and cloud-based traffic  
4. Increase scrutiny on newly created accounts  
5. Use payment outcomes (chargebacks/refunds) as feedback signals  
6. Evolve the rule-based system into a machine learning model  


## 🛠️ The Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Google Colab


## 📁 Project Structure

- **Fraud_Case_Study.ipynb** Main analysis and business insights  
- **Fraud_Risk.ipynb** Synthetic dataset generator  
- **subscription_fraud_dataset.csv** Dataset used for analysis  


## ▶️ How to Run

You can run this project directly in Google Colab:

1. Open `Fraud_Case_Study.ipynb`
2. Run all cells from top to bottom
3. No manual dataset upload required (data is loaded via GitHub)
## 📉 Model Overview

A simple logistic regression model was trained to predict fraud likelihood using features such as:

- accounts_per_device
- refund_count_90d
- trial_used_before
- network type flags
- risk signals

**Model Accuracy: ~98%**


## 🔮 Future Work

- Implement advanced machine learning models (XGBoost, Random Forest)
- Add behavioral signals (session velocity, login frequency)
- Integrate real world datasets where available
- Build a real time fraud scoring API


## 📚 References

- PYMNTS Fraud Report:  
  https://www.pymnts.com/wp-content/uploads/2021/11/PYMNTS-Beyond-eCommerce-Fraud-November-2021.pdf  

- Stripe Fraud Prevention Overview:  
  https://stripe.com/radar  


## 💡 About This Project
This project was built to focus on solving real business problems using data for the health, fitness, and tech industry.
