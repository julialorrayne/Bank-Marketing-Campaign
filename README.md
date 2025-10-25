# Bank-Marketing-Campaign

## Background and Overview
This project analyzes a bank marketing dataset containing historical data from May 2008 to November 2010, collected from direct phone-call campaigns conducted by a Portuguese banking institution.  
The primary objective is to identify which types of customers are most likely to subscribe to a term deposit and why, by applying both descriptive and predictive analytics techniques.

Through this analysis, we uncover behavioral and financial patterns that influence client decisions, translating findings into data-driven recommendations for campaign targeting, timing, and engagement.  
Ultimately, the goal is to help the bank optimize marketing resources, personalize outreach strategies, and increase ROI.

**Tools Used:** Python (Pandas, NumPy, Scikit-learn, Plotly, Seaborn, Matplotlib)

**Techniques:**  Exploratory Data Analysis (EDA) · Machine Learning Modeling · Correlation Analysis · Data Visualization · Clustering 

---

## Data Structure Overview
The dataset contains 45,210 records, each representing the outcome of a direct marketing campaign conducted by a Portuguese banking institution.  
Campaigns were performed through phone calls, and in many cases, multiple contacts with the same client were made to assess their interest in subscribing to a bank term deposit.

The dataset includes detailed information across three main dimensions:

- **Customer Demographics:** age, job type, marital status, education level  
- **Financial Attributes:** account balance, loan status, housing loan, default history  
- **Campaign Interactions:** call duration, number of contacts, previous campaign outcomes, and response to the current campaign (`y` = yes/no)

Data cleaning techniques included handling missing values and outliers, validating data types, removing duplicates, and eliminating irrelevant variables to ensure data quality and consistency.

> The original dataset can be found [here](https://archive.ics.uci.edu/ml/datasets/Bank+Marketing).

---

## Executive Sumamary

---

## Key Insights  

### Call Duration and Balance Influence on Subscription Likelihood

![scatterplot - duration vs balance](https://github.com/julialorrayne/Projects-images/blob/main/Bank-Marketing-Campaign/scatterplot%20-%20duration%20vs%20balance.png?raw=true)
Clients with longer call durations, particularly those lasting over 1,000 seconds (~16 minutes), show a higher likelihood of subscribing to a term deposit, especially within the low-to-moderate balance range (<$20k).

Longer conversations appear to positively influence subscription rates, suggesting that extended engagement increases client conversion.

---

### Financial Behavior by Education Level

![total balance by education](https://github.com/julialorrayne/Projects-images/blob/main/Bank-Marketing-Campaign/total%20balance%20by%20education.png?raw=true)

Clients with secondary education exhibit the highest total balances, followed by those with tertiary education, while clients with primary education show the lowest balances overall.

The trend suggests that clients with moderate educational backgrounds (secondary level) may represent the largest customer segment or hold stronger financial engagement with the bank.

Despite tertiary-educated clients typically earning more, their aggregate balances are lower, possibly due to diversified investments or reduced reliance on savings accounts.

Clients with only primary education might have limited earning potential, explaining their comparatively lower balances.

---

### Average Balance Trends Across Months  
![average balance across months](https://github.com/julialorrayne/Projects-images/blob/main/Bank-Marketing-Campaign/average%20balance%20across%20all%20months.png?raw=true)
There are noticeable fluctuations, with peaks in certain months like April and December, and a dip around July. Actionable Insight: Higher average balances in certain months could indicate periods where customers are more financially stable and likely to subscribe. Campaigns could be timed to align with these months (e.g., April and December) to target high-balance customers.

This chart illustrates **monthly fluctuations in clients’ average account balances**, providing insight into seasonal financial stability and potential campaign timing.  

- There are **noticeable peaks** in **April** and **December**, suggesting that customers tend to maintain **higher balances** during these months.  
- A **dip is observed around July**, indicating a potential mid-year decline in financial activity.  

- Higher balances in certain months (e.g., **April and December**) may correspond to **periods of higher financial stability**, when customers are more likely to commit to term deposits.  
- **Actionable Insight:** Align marketing campaigns or promotional offers with **high-balance months** to target financially ready customers.  
- For **lower-balance periods (like July)**, consider offering **short-term incentives or flexible deposit options** to encourage participation.  

---

### Impact of Past Campaign Outcomes on Current Success Rates

![success rate by previous campaign outcome](https://github.com/julialorrayne/Projects-images/blob/main/Bank-Marketing-Campaign/success%20rate%20by%20previous%20campaign%20outcome.png?raw=true)

The  chart compares success rates of the current campaign based on clients’ previous campaign outcomes. 

Clients who previously subscribed (success) exhibit a significantly higher success rate in the current campaign compared to those whose past outcomes were failures. This indicates a strong positive relationship between past and current campaign performance.

Clients with a successful previous outcome tend to subscribe again, suggesting brand trust and retention effects.

---

### Engagement Frequency and Its Impact on Campaign Success

![average previous calls by previous campaign](https://github.com/julialorrayne/Projects-images/blob/main/Bank-Marketing-Campaign/average%20previous%20calls%20by%20previous%20campaign.png?raw=true)  

This chart shows the average number of calls associated with those outcomes.

A higher average number of calls is observed among successful previous campaigns, implying that consistent engagement and follow-up communication may increase conversion likelihood.

Conversely, failed past campaigns correspond with low success rates and minimal call activity, highlighting the importance of maintaining customer relationship continuity across campaigns.

---

### Impact of Previous Campaign Success on Current Subscription Rate  
![subscription rate by previous campaign](https://github.com/julialorrayne/Projects-images/blob/main/Bank-Marketing-Campaign/subscription%20rate%20by%20previous%20campaign.png?raw=true)

The subscription rate is substantially higher (60%) for clients who subscribed in previous campaign compared to those who did not (~10%). This suggests that clients who have subscribed before are more confident or loyal, increasing their likelihood of subscribing again.  

  - Implement **personalized follow-ups** for previously successful clients to maintain engagement.  
  - Use **past campaign success** as a predictor in future models for improved targeting and efficiency.  

---

![customer segmentation - likelihood to subscribe](https://github.com/julialorrayne/Projects-images/blob/main/Bank-Marketing-Campaign/customer%20segmentation%20-%20likelihood%20to%20subscribe.png?raw=true)


![average subscription rate by cluster](https://github.com/julialorrayne/Projects-images/blob/main/Bank-Marketing-Campaign/average%20subscription%20rate%20by%20cluster.png?raw=true)

The clustering model segmented clients by Age, Call Duration, and Account Balance to identify patterns in subscription behavior.  

**Cluster 2 Profile — Highly Likely to Subscribe:**  
- **Average Age:** 41  
- **Average Balance:** ≈ $1,428  
- **Average Call Duration:** ≈ 10 minutes  
- **Average Calls During Campaign:** ≈ 2  
- **Average Contacts Before Campaign:** ≈ 1.2  
- **Subscription Rate:** 0.96 (**very likely to subscribe**)  

Cluster 2 represents the most responsive and engaged customer group, characterized by moderate balances and longer call durations.  
Their behavior suggests high receptivity to personalized and follow-up marketing.  
**Recommendation:** Future campaigns should **prioritize Cluster 2 clients** using tailored communication to maximize conversion and ROI.  

---

![subscription rates accross all months](https://github.com/julialorrayne/Projects-images/blob/main/Bank-Marketing-Campaign/subscription%20rates%20accross%20all%20months.png?raw=true)

The line chart illustrates monthly variations in subscription rates, highlighting seasonal fluctuations throughout the year.  

- Peaks in subscription activity occur in April (Month 4), May (Month 5), June (Month 6), and August (Month 8).  
- Drops are observed in March, July, and September, suggesting periods of lower customer engagement or interest.  

- Subscription behavior appears seasonally influenced, with stronger performance in spring and mid-summer months.  
- Declines later in the year may indicate campaign fatigue, reduced financial flexibility, or less marketing activity during those months.  
- **Recommendation:**  
  - Adjust marketing efforts by **intensifying outreach or offering targeted promotions** during low-performance months (e.g., March, July, September).  
  - Consider **seasonal campaign planning** to align promotional strategies with months showing historically higher engagement.  

---

#### High-Probability Segment Summary  

| Metric | Duration (seconds) | Previous Contacts | Age (years) | Balance ($) | Month of Contact |
|:--|--:|--:|--:|--:|--:|
| **Count** | 173 | 173 | 173 | 173 | 173 |
| **Mean** | **656** | **2.3** | **41** | **1,863** | **6.5** |
| **Standard Deviation** | 437.4 | 2.6 | 15.5 | 2,528.4 | 3.2 |
| **Minimum** | 152 | 0 | 18 | -887 | 1 |
| **25th Percentile** | 301 | 0 | 32 | 281 | 4 |
| **Median (50th)** | 475 | 2 | 42 | 926 | **6** |
| **75th Percentile** | 892 | 3 | 55 | 2,239 | 9 |
| **Maximum** | 2,062 | 12 | 83 | 16,517 | 12 |

The summary above highlights clients with the highest likelihood to subscribe based on key variables such as call duration, previous contacts, age, balance, and month of contact.  

- 171 clients are classified as highly likely to subscribe.  
- Call Duration: Mean of 656 seconds — longer calls correlate with higher subscription probability.  
- Previous Contacts: Average of 2.3 interactions — repeated engagement increases the likelihood of conversion.  
- Age: Mean of 41 years — middle-aged individuals are the most responsive segment.  
- Balance: Mean of $1,863 — high-probability clients generally maintain positive account balances.  
- Month of Contact: Median = Month 6 (June) — most high-probability contacts occurred in mid-year campaigns.  

High-probability subscribers are characterized by longer conversations, moderate positive balances, and repeat interactions, suggesting that personalized follow-ups with financially stable, mid-aged clients during mid-year campaigns can significantly increase term deposit conversions.
