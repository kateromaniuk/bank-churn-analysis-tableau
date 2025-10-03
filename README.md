# bank-churn-analysis-tableau

# 🏦 Project Background


This study project is based on the [Bank Customer Churn Dataset] from Kaggle. The dataset simulates a European retail bank with around 10,000 clients, offering personal accounts, savings, loans, and credit products in Germany, Spain, and France. This year, a major challenge for the company has been its customer churn – a big percentage of clients closed their accounts and left. As a data analyst, I was tasked with understanding churn patterns and finding the main risk factors.

The bank's key business metrics include:
- **Churn Rate:** 20.37% (2,037 clients out of 10,000 left in 2025)
- **Average Tenure:** 4.93 years for churned vs. 5.03 years for retained customers
- **Average Balance:** €91K for churned vs. €73K for retained customers
- **Products per Customer:** 1.48 for churned vs. 1.54 for retained customers

Applying descriptive analytics techniques, I discovered which customer groups are most likely to leave and where retention efforts should be focused.

Insights and recommendations are provided on the following key areas:
- **1. Geography**
- **2. Age**
- **3. Credit Score**
- **4. Balance** 

⭐️ An interactive Tableau dashboard used to report and explore churn drivers can be found here: [View Dashboard on Tableau Public](https://public.tableau.com/app/profile/kateryna.romaniuk/viz/BankChurnRateAnalysis_17577783591580/ChurnDashboardLight)



# Data Structure & Initial Checks
The dataset simulates a bank CRM system with the following key fields:
- *CustomerID*  – unique customer identifier
- *Country* – customer’s country of residence
- *Age* – grouped into categories for analysis
- *CreditScore* – grouped from Very Low (300–499) to Very High (800–850)
- *Balance* – grouped into balance ranges (€0, ≤25K, 25–75K, 75–125K, 125–200K, 200K+)
- *Tenure* – number of years a customer has been with the bank
- *Products* – number of products used (credit card, savings, loan, etc.)
- *Churn* – binary indicator (1 = churned, 0 = retained)

Initial checks included ensuring consistent currency formatting (€, thousands), checking for missing values, and validating customer counts across demographics.



# Executive Summary
Three main insights for stakeholders, they are:
1. Germany has the highest churn rate (32.4%), almost double Spain and France.
2. Middle-aged customers (46–65) are leaving at the highest rates (≈50%), highlighting a retention issue in the bank’s most financially valuable segment.
3. Customers with either very low balances (≤25K) or very high balances (200K+) are more likely to churn, showing that both ends of the wealth spectrum feel underserved.



# Insights Deep Dive
### 1. Geography

* 32.4% of German customers churned. This percentage was far smaller in Spain in France - both countries had about 16% of customers who left.
This suggests operational, cultural, or service issues specific to the German market.

![Visualization: Churn by Country](https://github.com/kateromaniuk/bank-churn-analysis-tableau/blob/main/churn%20by%20country.png?raw=true)

### 2. Age
* 46–55: Highest churn at 50%, followed by 56–65 at 48.5%.
* Younger groups (18–35) churn much less (≈8%).
This indicates the bank is losing established, mid-life customers who typically hold larger balances.

![Visualization: Churn by Age](https://github.com/kateromaniuk/bank-churn-analysis-tableau/blob/main/churn%20by%20age.png?raw=true)

### 3. Credit Score
* Churn is relatively stable across credit scores (19–24%).
* Customers with very low credit scores (300–499) show the highest churn (23.7%).
Suggests churn is not strongly credit-score driven, but slightly worse at the bottom of the range.

![Visualization: Churn by Credit Score](https://github.com/kateromaniuk/bank-churn-analysis-tableau/blob/main/churn%20by%20credit%20score.png?raw=true)

### 4. Balance
* Customers with ≤€25K balances churned at 66.7%.
* Customers with €200K+ balances churned at 55.9%.
* Mid-range balances (25K–200K) have much lower churn (~23%).
This indicates the bank is failing both low-income and high-net-worth clients, though for different reasons (possibly poor benefits for the wealthy, lack of incentives for small savers).

![Visualization: Churn by Balance](https://github.com/kateromaniuk/bank-churn-analysis-tableau/blob/main/churn%20by%20balance.png?raw=true)



# Recommendations
1. Germany Market Strategy: Investigate service gaps in Germany (e.g., product offerings, customer service, branch coverage). Consider targeted retention campaigns.
2. Middle-Aged Client Retention: Launch loyalty programs for 45–65-year-olds, emphasizing better interest rates, financial advisory services, or bundled products.
3. Low-Balance Customers: Improve accessibility (e.g., no-fee accounts, digital services) to encourage retention.
4. High-Balance Customers: Create premium banking services with personalized account managers and exclusive benefits to reduce churn.
5. Proactive Monitoring: Use predictive churn models to flag at-risk customers early (based on tenure, balance, and age group) and intervene with tailored offers.



# Assumptions and Caveats
- The dataset is simulated and anonymized; real-world results may vary.
- Country churn differences may reflect sampling bias rather than true market behavior.
- The dataset does not capture customer satisfaction scores or transaction-level data, which would improve explanatory power.
- Churn is analyzed on 2025 data only; time-series trends are not available.
