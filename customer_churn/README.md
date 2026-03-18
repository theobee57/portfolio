# Customer Churn Risk Analysis

## Overview

Customer retention is critical for sustainable business growth. This project analyzes customer behavior to identify key drivers of churn and highlight actionable strategies to improve retention.

The analysis focuses on understanding how contract types, tenure, pricing, and service features influence customer churn risk.

---

## Business Problem

Which customers are most likely to churn, and what factors contribute most to churn risk?

Understanding these drivers enables businesses to:
- reduce customer loss
- improve retention strategies
- increase lifetime customer value

---

## Dataset

The dataset contains customer-level information including:

- Customer demographics (gender, senior citizen, dependents)
- Account details (tenure, contract type, payment method)
- Services used (internet service, tech support, online security)
- Financial data (monthly and total charges)
- Target variable: **Churn (Yes/No)**

---

## Tools Used

- Python
- pandas
- numpy
- matplotlib
- DataLab (DataCamp)

---

## Analysis Approach

The analysis was conducted in the following steps:

1. Data cleaning (handling missing values and duplicates)
2. Creation of churn indicator variable
3. Exploratory data analysis (EDA)
4. Segmentation of customers by:
   - contract type
   - tenure
   - pricing
   - service usage
5. Identification of high-risk customer profiles

---

## Key Insights

### 1. Contract Type is the Strongest Driver of Churn

Customers on **month-to-month contracts** exhibit significantly higher churn rates compared to long-term contracts.

- Short-term commitment → higher likelihood to leave
- Long-term contracts → strong retention effect

---

### 2. Early Tenure Customers Are High Risk

Customers in their **first 12 months** show the highest churn probability.

- Indicates onboarding and early experience are critical
- Retention strategies should focus on the first year

---

### 3. Lack of Support Services Increases Churn

Customers without:
- **Tech support**
- **Online security**

are more likely to churn.

This suggests that value-added services improve retention.

---

### 4. Higher Monthly Charges Correlate with Higher Churn

Customers with higher monthly charges tend to churn more frequently.

- Potential price sensitivity
- Possible perception of low value for cost

---

### 5. High-Risk Customer Profile

The most at-risk customers typically have:

- Month-to-month contracts  
- Short tenure (< 12 months)  
- No tech support or online security  
- Higher monthly charges  

---

## Business Recommendations

Based on the analysis, the following actions are recommended:

### 1. Target Month-to-Month Customers
- Offer incentives to switch to long-term contracts
- Introduce loyalty discounts

### 2. Strengthen Early Customer Engagement
- Improve onboarding experience
- Introduce check-ins during first 3–6 months

### 3. Bundle Value-Added Services
- Include tech support or security features in packages
- Promote these services to high-risk customers

### 4. Review Pricing Strategy
- Evaluate pricing for high-cost segments
- Offer tiered pricing or bundled discounts

### 5. Proactive Retention Campaigns
- Identify high-risk customers early
- Trigger targeted retention offers

---

## Sample Visualizations

### Churn by Contract Type

![Churn by Contract](visuals/churn_by_contract.png)

---

### Churn by Tenure

![Churn by Tenure](visuals/churn_by_tenure.png)

---

## Project Structure

```text
customer-churn-analysis
│
├── README.md
├── data
├── notebooks
└── visuals
````

---

## Portfolio Value

This project demonstrates:

* End-to-end data analysis using Python
* Customer segmentation and behavioral analysis
* Identification of business risk drivers
* Translation of data into actionable business insights
* Clear communication of findings for decision-making

---

## Next Steps (Optional Enhancements)

* Build a churn prediction model (logistic regression)
* Perform feature importance analysis
* Create an interactive dashboard (Tableau or Power BI)

---

````

---
