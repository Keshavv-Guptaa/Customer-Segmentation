# Customer-Segmentation
This repository contains customer segmentation based on items purchased and transaction history.


## EDA
( 5 numerical and 3 categorical features )
1. 50.5% of entries were duplicated
2. Maximum transactions were from the United Kingdom
3. Missing values in Item Description
4. 25900 transactions by 4373 users
5. Highly skewed Cost per item
6. Negative values for Number of items and cost per item

## Data Cleansing
1. Removed duplicate entries
2. Removed illogical( negative or extremely high values ) entries for Number of items and cost  per item
3. Removed transactions which were not between the period Feb 2018 to Feb 2019

## Feature Engineering
1. Created a new feature of total amount by the product of Number of items and cost per item
2. Converted the Transaction time from string to DateTime object

## RFM Modelling for customer segmentation
1. Created three features Recency = Latest Date - Last transaction, Frequency = no. of transaction(s), Monetary = Sum of the total amount, then split into four segments using quantiles and assigned it to three new features R, F, and M
2. Calculated RFM score by adding R, F, and M and assigned Loyalty Level of 'Platinum', 'Gold', 'Silver', 'Bronze' to each customer
3. Applied log transformation to recency, frequency, and monetary values as they were not normally distributed

## K-Means Clustering
1. Used the elbow method to find the optimal number of clusters by WCSS values.
2. Finally trained the model with 4 clusters and assigned a specific color to each
