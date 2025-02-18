# Analytic Report for National Clothing Company

[Project link](https://app.powerbi.com/view?r=eyJrIjoiZWVmZDliNTQtZjYzNC00NGI2LTlkYmYtZmVjZDZkMzIyZDc1IiwidCI6Ijk2ZDUwZjcyLWE2MGMtNDgwOS1iNGI1LTIwYjQ5NDUxNjFhZSJ9&pageName=63505591280cd50d404d)

This project focuses on leveraging data analytics to generate insights for targeted marketing campaigns. The project addresses historically low customer engagement attributed to limited marketing initiatives, aiming to revive and improve sales through personalized outreach strategies informed by behavioral patterns and purchasing trends.

## Data Sources
* Average Temperatures by State
* Census Data
* Customer List
* Purchase List
* State List

## Analysis Questions
1. What is the correlation (R2 value) between sales and income?
2. What is the correlation (R2 value) between customer ratings and product return rate?
3. What are the linear regression formulas to predict customer income from customer sales?
4. Which customer do you predict has the highest income?
5. Which product will be advertised the most?

## Wrangling
* Used Power Query to split the columns under the Product Inventory table using a delimiter. More transformations such as changing data type, extracting dates and merging columns were used.
* For the Purchase List table, unpivoting all asides the ID column was done to standardize the table

## Analysis and Visualisation
The data schema here shows all the connections as needed
![Data Schema](images/dSchema.png)

The report consists of the following pages:

1. Home
![HOME](images/HomePage.jpeg)

2. Predicted Customer Income Summary
![Predicted Income Summary](images/CustomerIncomeSummary.jpeg)

* Using each state’s average Income and each state’s average Last 6 Months of Purchase, a simple Regression formula helped predict each customer’s income.

* The scatter plot shows a strong positive correlation of .78 between the Average Income and the Average Last 6 Months of Purchases.

* The linear regression formula is Y = .01X + -722.14.
where
* X represents the Predicted Income
* Y represents the Last 6 Months of Purchases
 
4. Products Summary
![Products Summary](images/ProductSummary.jpeg)

In this page, 
* There is a strong negative correlation of .69 between the Customer Rating and the Return Rate.
* A few of the best products with both highest Customer Rating and also, lowest Return Rate are 1. The Chronograph Watch, 2. Long Dress, and 3. Leather Sneakers. All of these products are considered to be of medium cost as compared to the other products sold.
* Winter gloves have the highest return rate and one of the lowest customer ratings.
* Leather Bags are the most expensive product offered and they also have pretty high return rate and low customer rating. So also, we have a very large inventory value for these same Leather Bags. 


6. Customer Summary
![Customer Summary](images/CustomerSummary.jpeg)

Here, we discovered these important points:
* We predict customer `Jon Little` to have the highest income of $488,742.15.
* Customers tend to spend more towards the end of the year (Ember months).
* Most of our customers are from California, Florida and Texas.
* Most of our customers fall under the age range of 40-49 year olds.

 
7. AdHoc Analysis
![AdHoc Summary](images/AdHoc%20Analysis.jpeg)
