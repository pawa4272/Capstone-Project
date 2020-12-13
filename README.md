![](https://i.chzbgr.com/full/9034875648/h6A5212A2/made-into-a-meme-captioned-the-difference-between-meme-and-you-is-that-i-make-these-look-good)

# Improving Instacart 1 customer at a time via Basket Analysis
by Paulette Rodrigues

# Table of Contents

- [Introduction](project-title)
- [Introduction](#introduction)
- [Data](#data)
- [Modeling](#modeling)
- [Next Steps](#next-steps)

# Introduction

Instacart was launched in June 2012 as a grocery delivery and pick-up service. It is essentially a delivery platform that partners with retailers across the United States and Canada to provide food products to their customers. By 2017 the retailer Whole Foods was responsible for more than 10 % of there sales
Their competitor Amazon acquired Whole Foods, for $13.7 billion in August 2017 … putting them now in second to Amazon  (Tom’s Guide).For the past three years Instacart was able to maintain and retain their market share; based on 2019 figures, membership has tripled in 2020 

How can Instacart’s customers decrease the time spent by to complete their full order, improve their online experience and have them return as customers post Covid19? 

# Problem Statement 

To improve customer's experience and reduce the time needed to place an order, Instacart can then direct customers to the best retailer that would be able to fulfill thier order. This Project serve to predict which products a customer may reorder in their next purchase. 

# Data

The dataset is a relational set of files describing customers' orders over time, and can be found at the following location: https://www.kaggle.com/c/instacart-market-basket-analysis/data.


•Data was
aggregated to create one row per customer’s per item purchased


•Aggregation was done based on the
following conditions:


•By items purchased from 
all customer’s orders


•By items purchased from the last 5 orders of the
customer


•Department of the item was also
kept as the natural category of the items


•Null values were set to 0

### Data Dictionary

Final aggregated dataset used.

|Feature|dtype|Description|
|---|---|---|
|user_product |object| Concatenation of user id and product is |
|department| object |Department in which the product belongs |
|times_ordered | int64 | The number of times the user purchase the product in their prior orders |
|total_orders| int64 | The number of times the user shopped on Instacart |
|pct_reorder| float64  |times_ordered / total_orders |
|max_days_bet| float64 |Maximum number of days between customer's orders|
|avg_days_bet|float64|Avgerage number of days between customer's orders|
|min_reorder_days|float64|Minimum reorder days between customer's orders|
|max_reorder_days|float64|Maximum reorder days between customer's orders|
|avg_reorder_days|float64|Average reorder days between customer's orders|
|target|int64|Reordered, for train/test 1 - Yes, 0 - No|
|last5_times_item_pur|float64|The number of times the user purchase the product in their last 5 orders |
|last5_total_orders|float64|The number of times the user shopped on Instacart (last 5 orders), if users order; 5 if >= 5 else number of orders |
|last5_pct_order|float64|last5_times_item_pur / last5_total_orders|
|min_days_5odrs|float64|Minimum number of days between customer's orders|
|max_days_5odrs|float64|Maximum number of days between customer's orders|
|avg_days_5odrs|float64|Average number of days between customer's orders|
|min_reorder_5days|float64|Minimum number of days between customer's orders|
|max_reorder_5days|float64|Maximum number of days between customer's orders|
|avg_reorder_5days|float64|Average number of days between customer's orders|
|avg_items_ordered|float64|Average number of items ordered in a customer's history|
|last5_avg_items|float64|Average number of items ordered in a customer's last 5 purchase|


# Modeling

Since the data set is imbalance, a sample of 500,000 rows were selected and then SMOTE was applied to generate artificual rows and balance the binary classification. Several binary classification models were then generated to identify the best model

- Best Model: Logistic Regression
- Sensitivity: 0.6896 
- ecificity: 0.7388

# Next Steps

- Train the data with other models
- Apply grid search to the best 3 models
- Add / remove other features to get the optimal solution
