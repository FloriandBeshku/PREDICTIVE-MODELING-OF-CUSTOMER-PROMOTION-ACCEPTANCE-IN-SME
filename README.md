# Predictive Modeling of Customer Promotion Acceptance
**Floriand Beshku | 2026**

This project demonstrates how data can be used to improve promotional decision-making by replacing intuition-based marketing with an objective, data-driven approach. Rather than relying on broad assumptions, this analysis predicts which customers are most likely to accept a promotion and explains which specific behaviors meaningfully influence that decision.

## Business Problem
In many small and medium-sized businesses, promotional decisions are driven by intuition, leading to inefficient use of marketing resources. Promotions are frequently sent to large segments without evidence of who is most likely to respond, resulting in wasted spend and missed opportunities.
* **Identify High-Potential Customers:** Pinpoint who is most likely to accept an offer before allocating resources.
* **Reduce Wasted Outreach:** Minimize sending promotions to segments with little intention of joining.
* **Optimize Conversion Rates:** Justify promotional decisions with measurable evidence rather than assumptions.

## Technical Stack
* **Language:** Python
* **Environment:** Anaconda / Jupyter Notebook
* **Libraries:** Pandas, NumPy, Scikit-Learn, Statsmodels, Matplotlib, Seaborn
* **Modeling:** Logistic Regression

## Methodology & Workflow
I followed a structured data science workflow to ensure reliability and interpretability:
1. **Data Preparation:** Cleaned a dataset of 5,000 gym customers and created indicator variables for categorical features.
2. **Data Partitioning:** Split the data into Training (50%), Validation (30%), and Test (20%) sets.
3. **Predictive Modeling:** Developed a Logistic Regression model to estimate the probability of acceptance for each customer.
4. **Threshold Analysis:** Evaluated the performance of a conservative 0.50 threshold versus a growth-oriented 0.30 threshold to align with business goals.
5. **Model Optimization:** Applied statistical variable selection (p-values) to reduce the model to the most significant predictors.

## Key Results & Business Insights
The analysis identified several "warm lead" behaviors that significantly increase the likelihood of promotion acceptance:
* **Trial Class Attendance (+0.94):** Customers who attended a trial class are much more likely to accept the promotion.
* **Tour Completion (+0.74):** Completing a gym tour is a high-impact indicator of interest.
* **Referral Source (+0.51):** Customers coming through referrals show substantially higher responsiveness.
* **Digital Engagement:** Recent SMS clicks (+0.15) and email opens (+0.08) serve as reliable triggers for outreach.

## Practical Application
A reduced version of the model achieves comparable performance while relying on fewer variables, making it easier to deploy in real-world CRM or marketing automation platforms.

**Reduced Logistic Regression Formula:**
$$p = \frac{1}{1 + \exp(-(-3.49 - 0.02(\text{Days Since Visit}) + 0.94(\text{Trial Class}) + 0.74(\text{Tour}) + 0.51(\text{Referral}) + \dots))}$$
