# Improving Instacart 1 customer at a time via Basket Analysis
by Paulette Rodrigues

# Table of Contents

- [Introduction](project-title)
- [Introduction](#introduction)
- [Data](#data-cleaning)
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



# Modeling

- Best Model: Logistic Regression
- Sensitivity: 0.6896 
- ecificity: 0.7388

# Next Steps

- Train the data with other models
- Apply grid search to the best model
- Add / remove other features to get the optimal solution
