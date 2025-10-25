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
![scatterplot - duration vs balance](https://github.com/julialorrayne/Projects-images/blob/main/Bank-Marketing-Campaign/scatterplot%20-%20duration%20vs%20balance.png?raw=true)
Clients with longer call durations, particularly those lasting over 1,000 seconds (~16 minutes), show a higher likelihood of subscribing to a term deposit, especially within the low-to-moderate balance range (<$20k).

---

Interpretation:

Longer conversations appear to positively influence subscription rates, suggesting that extended engagement increases client conversion.

![total balance by education](https://github.com/julialorrayne/Projects-images/blob/main/Bank-Marketing-Campaign/total%20balance%20by%20education.png?raw=true)
Insight:
Clients with secondary education exhibit the highest total balances, followed by those with tertiary education, while clients with primary education show the lowest balances overall.

Interpretation:

The trend suggests that clients with moderate educational backgrounds (secondary level) may represent the largest customer segment or hold stronger financial engagement with the bank.

Interestingly, despite tertiary-educated clients typically earning more, their aggregate balances are lower, possibly due to diversified investments or reduced reliance on savings accounts.

Clients with only primary education might have limited earning potential, explaining their comparatively lower balances.

---

![success rate by previous campaign outcome](https://github.com/julialorrayne/Projects-images/blob/main/Bank-Marketing-Campaign/success%20rate%20by%20previous%20campaign%20outcome.png?raw=true)
![average previous calls by previous campaign](https://github.com/julialorrayne/Projects-images/blob/main/Bank-Marketing-Campaign/average%20previous%20calls%20by%20previous%20campaign.png?raw=true)

According to the first bar chart, the success rate for currrent campaign is high when previous campaign was a success, while the success rate is low when previous campaign was a failure. This indicates a strong relationship between sucessful past campaigns and likelihood of success in current campaign.
Most of the clients that previously subscribed tend to subscribe again, which can be due to retention and loyalty. 
According to the second bar chart, the successful outcome for previous campaign has a higher average number of previous calls compared to failure.

![customer segmentation - likelihood to subscribe](https://github.com/julialorrayne/Projects-images/blob/main/Bank-Marketing-Campaign/customer%20segmentation%20-%20likelihood%20to%20subscribe.png?raw=true)
![average subscription rate by cluster](https://github.com/julialorrayne/Projects-images/blob/main/Bank-Marketing-Campaign/average%20subscription%20rate%20by%20cluster.png?raw=true)

Cluster 2: Highly likelihood to subscribe.

Average age: 41
Balance: ~1428
Call duration: ~10 mins
Number of calls during campaign: ~2
Number of contacts before this campaign: 1.22
Subscription rate: 0.96(very likely to subscribe)
The marketing campaign should focus on clients from Cluster 2.



![subscription rates accross all months](https://github.com/julialorrayne/Projects-images/blob/main/Bank-Marketing-Campaign/subscription%20rates%20accross%20all%20months.png?raw=true)
Subscription Rates Across All Months (Line Chart) There are peaks in April (Month 4), May (Month 5), June (Month 6), and August(Month 8)
There is a drop in Mach, July, September subscription rates, which might indicate that customers are less interested during the end of the year.
Should adjust campaigns or consider offering seasonal promotions in the months with drops to increase subscriptions.


![high probability segment summary](https://github.com/julialorrayne/Projects-images/blob/main/Bank-Marketing-Campaign/high%20probability%20segment%20summary.png?raw=true)
171 clients are highly likely to subscribe.
duration- Call duration mean: 656 seocnds. Clients with longer call durations are more likely to subscribe.
previous- Number of previous contacts mean: 44. Clients who are more likely to subscribe tend to have more previous interactions.
age - age mean: 41 years. The mean age represents midle-aged individuals.
balance - account balance mean: $1,863. High probability clients have positive balances.
month - month of contact median: most contacts occurred in month 6 or later.


![subscription rate by job and education](https://github.com/julialorrayne/Projects-images/blob/main/Bank-Marketing-Campaign/subscription%20rate%20by%20job%20and%20education.png?raw=true)
Individuals with tertiary education have higher subscription rates.
Students exhibit the highest subscription rate, followed by retired individuals and those in management roles.
Customized marketing strategies messages: . technicians and entrepreneurs: messaging emphasizing financial growth or stability.
. unemployed and housemaid: campaigns offering financial inclusion or support.


![subscription rate by previous campaign](https://github.com/julialorrayne/Projects-images/blob/main/Bank-Marketing-Campaign/subscription%20rate%20by%20previous%20campaign.png?raw=true)

The subscription rate is substantially higher (around 0.6 or 60%) for clients who subscribed in previous campaign. This indicates that prior successful engagement builds customer loyalty or confidence in subscribing again.

![average balance across months](https://github.com/julialorrayne/Projects-images/blob/main/Bank-Marketing-Campaign/average%20balance%20across%20all%20months.png?raw=true)
There are noticeable fluctuations, with peaks in certain months like April and December, and a dip around July. Actionable Insight: Higher average balances in certain months could indicate periods where customers are more financially stable and likely to subscribe. Campaigns could be timed to align with these months (e.g., April and December) to target high-balance customers.
