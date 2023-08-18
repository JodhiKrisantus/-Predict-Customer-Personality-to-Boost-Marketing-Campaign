# Predict Customer Personality Marketing Campaign Clustering
**Column Description**
- `ID` = Customer's id
- `Year_Birth` = Customer's year of birth
- `Education` = Customer’s level of education
- `Marital_Status` = Customer’s marital status
- `Income` = Customer’s yearly household income
- `Kidhome` = Number of small children in customer’s household
- `Teenhome` = Number of teenagers in customer’s household
- `Dt_Customer` = Date of customer’s enrolment with the company
- `Recency` = Number of days since the last purchase
- `MntWines` = Amount spent on wine products in the last 2 years
- `MntFruits` = Amount spent on fruits products in the last 2 years
- `MntMeatProducts` = Amount spent on meat products in the last 2 years
- `MntFishProducts` = Amount spent on fish products in the last 2 years
- `MntSweetProducts` = Amount spent on sweet products in the last 2 years
- `MntGoldProds` = Amount spent on gold products in the last 2 years
- `NumDealsPurchases` = Number of purchases made with discount
- `NumWebPurchases` = Number of purchases made through company’s web site
- `NumCatalogPurchases` = Number of purchases made using catalogue
- `NumStorePurchases` = Number of purchases made directly in stores
- `NumWebVisitsMonth` = Number of purchases made through company’s web site
- `AcceptedCmp3` = 1 if customer accepted the offer in the 3rd campaign, 0 otherwise
- `AcceptedCmp4` = 1 if customer accepted the offer in the 4th campaign, 0 otherwise
- `AcceptedCmp5` = 1 if customer accepted the offer in the 5th campaign, 0 otherwise
- `AcceptedCmp1` = 1 if customer accepted the offer in the 1st campaign, 0 otherwise
- `AcceptedCmp2` = 1 if customer accepted the offer in the 2nd campaign, 0 otherwise
- `Complain = 1` if customer complained in the last 2 years
- `Z_CostContact` = Cost to contact a customer
- `Z_Revenue` = Revenue after client accepting campaign
- `Response` = 1 if customer accepted the offer in the last campaign, 0 otherwise


## Problem Statement
*In an increasingly competitive business era, deep understanding of customer behavior and personality has become crucial for companies that want to grow and succeed. In this context, it is important for companies to be able to identify the characteristics and preferences of potential customers who can become loyal customers in the future. Through analyzing historical data from past marketing campaigns, companies can improve campaign efficiency and direct their efforts towards the right customers, with the aim of increasing transactions and interactions on the company's website.*

## Objective
Identify potential customers to make purchases on the website, so as to reduce company expenses and increase revenue

# Quick Result 
## Income Distribution Against Conversion Rate
<img src="https://github.com/JodhiKrisantus/Predict-Customer-Personality-Marketing-Campaign-Clustering/blob/master/Resource%20image/Distribution%20Income%20-%20Conversion%20Rate.png">

- The conversion rate for each customer is usually influenced by the amount of income that customer has. meaning that there is a positive correlation, where the higher the level of customer income, the higher the conversion rate.

- Customers with high levels of income (Income) tend to have high purchasing power, so it is recommended to provide campaigns to customers with high income segmentation so that revenue can be increased and can make costs efficient.

## Effect of Education Level on Conversion Rate
<img src="https://github.com/JodhiKrisantus/Predict-Customer-Personality-Marketing-Campaign-Clustering/blob/master/Resource%20image/Education%20-%20Conversion%20rate.png">

Customer yang tingkat pendidikannya SMA memiliki rata rata accept campaign yang paling rendah, sedangkan customer dengan education S3 memiliki rata rata accept campaign terbesar. Faktor penyebabnya mungkin karena customer yang tingkat pendidikannya hanya mencapai SMA mempunyai kesulitan finansial dalam pekerjaannya, jika dibandingkan dengan customer dengan education S3 yang memiliki pekerjaan yang lebih baik sehingga income lebih besar. 

## K-Means Clustering Result
<img src="https://github.com/JodhiKrisantus/Predict-Customer-Personality-Marketing-Campaign-Clustering/blob/master/Resource%20image/Clusters%20result.png">

## Cluster Overview
<img src="https://github.com/JodhiKrisantus/Predict-Customer-Personality-Marketing-Campaign-Clustering/blob/master/Resource%20image/Cluster%20summary.png">

There are 3 clusters:

- Cluster 0 ( `Low Spender` ): Is a customer group that provides the smallest income for the company. This customer group has the greatest interest in visiting the company's website (7 days a month), but it is very rare to shop so it has the lowest conversion rate. This customer group is also the least likely to accept the campaigns offered by the company.
- Cluster 1 ( `Mid Spender` ). This customer group provides the second largest revenue for the company. This customer group also has the second largest interest in visiting the website (5 days a month). Even so, the conversion rate in this group is higher than the Low Spend group, which shows that these customers are more effective in shopping. The campaign acc level in the Mid Spend Group is also greater than the Low Spend group.
- Cluster 2 ( `Potential` ). This customer group provides the highest income for the company. This group rarely visits websites, but has high purchasing power, so this Potential group has the highest conversion rate compared to other groups. This group also has the most potential in responding to campaigns provided by the company.

## Average purchases per cluster by product category.
<img src="https://github.com/JodhiKrisantus/Predict-Customer-Personality-Marketing-Campaign-Clustering/blob/master/Resource%20image/Avg%20purchases%20per%20cluster%20by%20product%20category.png">
### Average Purchases Per Cluster

1. `Potential Customer` : has a habit of buying products directly at stores or stores with an average purchase of 8 times per month. Potential Customer Group, this group visits the website the least often compared to the Mid Spender and Low Spender Groups, but has the best potential to buy products through the website, especially from the Catalog and Web categories.
Recommendation : Since this group has the best potential to purchase products through websites, businesses should focus on improving the user experience on their online platforms. Make sure the website is easily accessible, responsive and user-friendly so that potential customers feel comfortable shopping online.

2. `Customer Mid Spender`: also has a habit of buying products directly at stores or shops with an average purchase of 7 times per month. This Mid spender customer group is most interested in buying products with Discount Vouchers compared to the Low Spender & Potential group.
Recommendation : Companies can focus on promotion and marketing with Discount Vouchers, because this group is interested in such offers. By providing attractive discounts or offers, the possibility of customers from this group to shop will increase.

3. `Low Spender Customer` : The Low Spender customer group also has a habit of buying products directly from stores, even though the Low Spender group has the highest number of website visits compared to other customer groups.
Recommendation: Companies can provide special incentives to encourage this customer group to shop more frequently, for example with a loyalty program or additional discounts for repeat purchases.

`Conclusion` : *For each customer group, the majority still use conventional shopping methods, namely through direct visits to stores. So companies need to analyze and optimize the user experience of using websites, such as admin services, ease of website navigation, clear product descriptions, etc.*


## Clusters Revenue
<img src="https://github.com/JodhiKrisantus/Predict-Customer-Personality-Marketing-Campaign-Clustering/blob/master/Resource%20image/Gmv%20per%20cluster.png">

Companies can target / focus on maintaining 'Potential' customer clusters, so the revenue received by customers from this cluster is around 762 million. The average income of companies originating from this potential cluster is dominated by customers in the elderly age category. However, in the Mid Spender Cluster, the highest income contributor is dominated by productive age customers. In fact, the elderly in the Mid Spender group have the lowest contribution to GMV revenue for the company.

`Recommendation` 
- The "Mid Spender Cluster" appears to be dominated by working age customers, who are the highest contributor to GMV revenue for the company. Companies must understand more about the preferences, needs, and motivations of customers within this group to maintain their contribution.
- Companies can collect customer data (not only age or product category, but can be in the form of data on what products each customer purchases) so that companies can provide a more personalized experience and according to the preferences of each customer group.
