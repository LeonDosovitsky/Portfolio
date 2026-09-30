# 🛒 Costco

**This project will be made using Python (pandas), Jupiter notebook and will be presented with TABLEAU.**

This project aims to analyze Costco's e-commerce sales to identify the following:
- The top 5 most popular items for each age group
- Total profit from 20+ item orders by male Costco members

## 📚 Table of Contents
- [Top 5](#Top-5-most-popular-items-for-each-age-group)
- [Total profit](#Total-profit-from-20-item-orders-by-male-Costco-members)
- [Dashboard](#dashboard)

## Top 5 most popular items for each age group

The first 5 rows reflect that the data does not have the same format. I will clean the age & gender columns by removing "years" and transforming Male/Female -> M/F.

![1](https://github.com/LeonDosovitsky/Images/blob/main/Images/costco_1.png?raw=true)

I extracted the maximum & minimum ages of customers, and created the following age groups: [18-29] [30-49] [50-65] [0]. The data from the age group 0 will be removed for this analysis in a future step.
<br><br>
I converted the age to Int64 since the age was a string and the column contains NaN values.

![2](https://github.com/LeonDosovitsky/Images/blob/main/Images/costco_2.png?raw=true)

I made some Left Joins to add the age group and product name to the orders.<br>
Removed all rows with age_group 0.

As a last step I created a new DataFrame with only the relevant data for my analysis and exported it as a .CSV file.

## Total profit from 20+ item orders by male Costco members

Taking the first part as a base template, I added a column with the rounded profit amount by item and a column with the total profit per row to account for multiple purchases of the same item in 1 order.

![3](https://github.com/LeonDosovitsky/Images/blob/main/Images/costco_3.png?raw=true)

I created and joined DataFrames for the total quantity ordered, the total profit for each order and for the gender of the account.

![4](https://github.com/LeonDosovitsky/Images/blob/main/Images/costco_4.png?raw=true)

For the last step I removed all orders with less than 20 items and orders without the gender set as "M".<br>
I exported the file as a .CSV

## 📊Dashboard
I made a simple TABLEAU dashboard to present the results of the analysis : [Tableau Dashboard](https://public.tableau.com/app/profile/leon.dosovitsky/viz/Costco_17891681902780/Dashboard1)

![5](https://github.com/LeonDosovitsky/Images/blob/main/Images/costco_5.png?raw=true)



