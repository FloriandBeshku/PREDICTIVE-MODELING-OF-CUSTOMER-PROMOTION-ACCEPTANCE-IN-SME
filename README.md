# Predictive Modeling of Customer Promotion Acceptance
**Floriand Beshku | [cite_start]2026** [cite: 1]

[cite_start]This project demonstrates how data can be used to improve promotional decision-making by replacing intuition-based marketing with an objective, data-driven approach[cite: 13]. [cite_start]Rather than relying on assumptions, this analysis predicts which customers are most likely to accept a promotion and identifies the specific behaviors that influence that decision[cite: 14].

## 📊 Business Problem
[cite_start]In many businesses, promotional decisions are driven by intuition, leading to inefficient use of marketing resources[cite: 30, 31]. [cite_start]This project addresses the lack of a reliable, data-driven method for targeting promotions[cite: 37].
* **Identify High-Potential Customers:** Pinpoint who is most likely to accept an offer before allocating resources[cite: 38].
* [cite_start]**Reduce Wasted Outreach:** Minimize sending promotions to segments with little intention of joining[cite: 32, 35].
* [cite_start]**Optimize Conversion Rates:** Justify promotional decisions with measurable evidence rather than assumptions[cite: 39].

## 🛠️ Technical Stack
* **Language:** Python [cite: 154]
* [cite_start]**Libraries:** Pandas, NumPy, Scikit-Learn, Statsmodels, Matplotlib, Seaborn [cite: 11]
* [cite_start]**Modeling:** Logistic Regression [cite: 127]



## 📈 Methodology & Workflow
[cite_start]I followed a structured data science workflow to ensure reliability and interpretability[cite: 20]:
1.  [cite_start]**Data Preparation:** Converted categorical variables into binary indicators and removed identifiers to avoid bias[cite: 85, 122].
2.  [cite_start]**Data Partitioning:** Split the 5,000-record dataset into Training (50%), Validation (30%), and Test (20%) sets[cite: 144, 145].
3.  [cite_start]**Predictive Modeling:** Utilized Logistic Regression to estimate the probability of acceptance for each customer[cite: 127, 129].
4.  [cite_start]**Threshold Analysis:** Evaluated the performance of a 0.50 threshold versus a growth-oriented 0.30 threshold[cite: 134, 137].
5.  [cite_start]**Model Optimization:** Applied statistical variable selection (p-values) to reduce the model to the 15 most significant predictors[cite: 139, 205].



## 🏆 Key Results & Business Insights
[cite_start]The final model identified several "warm lead" behaviors that significantly increase the likelihood of promotion acceptance[cite: 232]:
* [cite_start]**Trial Class Attendance (+0.94):** Customers who attended a trial class are much more likely to accept the promotion[cite: 162, 164].
* **Tour Completion (+0.74):** Completing a gym tour is a high-impact indicator of future acceptance[cite: 233].
* [cite_start]**Referral Source (+0.51):** Customers coming through referrals are substantially more responsive[cite: 167, 169].
* [cite_start]**Digital Engagement:** Active SMS clicks (+0.15) and email opens (+0.08) serve as reliable triggers for successful outreach[cite: 165, 166, 234].

## 🚀 Practical Application
[cite_start]The reduced model achieves comparable performance with fewer variables, making it easier to deploy in real-world CRM or marketing automation platforms[cite: 26, 245].

**Reduced Logistic Regression Formula:**
[cite_start]$$p = \frac{1}{1 + exp(-(-3.49 - 0.02(\text{Days Since Visit}) + 0.94(\text{Trial Class}) + 0.74(\text{Tour}) + 0.51(\text{Referral}) + \dots))}$$ [cite: 209]



### Strategic Recommendation
[cite_start]I recommend using the **30% probability threshold**[cite: 248]. [cite_start]Because the marginal cost of digital outreach (email/SMS) is low, this threshold captures significantly more potential members who would otherwise be missed under a stricter rule[cite: 189, 242, 243].
