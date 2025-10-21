# Bank-Marketing-Campaign

## Objective
Analyze a Portuguese bank’s marketing campaign data to understand **which customers subscribe to term deposits and why**, then translate findings into **actionable recommendations** for targeting, timing, and engagement.

---

**Target Question:** What factors (customer traits, timing, engagement) most influence subscription?

---

![scatterplot - duration vs balance](https://github.com/julialorrayne/Projects-images/blob/main/Bank-Marketing-Campaign/scatterplot%20-%20duration%20vs%20balance.png?raw=true)
Most clients have balances below $20000 and short call duration (less than 500 seconds, or 8 minutes).
The number of clients that subscribed to a term deposit is higher for low-to-moderate balances(below 20k) and call duration above 1000 seconds(~16 minutes)

![total balance by education](https://github.com/julialorrayne/Projects-images/blob/main/Bank-Marketing-Campaign/total%20balance%20by%20education.png?raw=true)
clients with secondary education have higher average annual balances

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
