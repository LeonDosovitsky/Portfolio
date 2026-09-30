# 🥤Coca-Cola

**This project's goal is to show an ETL pipeline with 3 different tools.**

This project aims to analyze sales and performance data to identify underperforming stores and Coca Cola products.
For this analysis, stores and Coca Cola products situated in the first quartile will be considered as underperforming.

## 📚 Table of Contents
- [Excel Power Query](#Excel-Power-Query)
- [SQL](#SQL)
- [Python](#python)

# Excel Power Query

I loaded my data into Power Query, promoted the first row to headers and changed my data to numbers.

![1](https://github.com/LeonDosovitsky/Images/blob/main/Images/excel_1.png?raw=true)

I added a Total Sales column that calculates the sum of all sales.

![2](https://github.com/LeonDosovitsky/Images/blob/main/Images/excel_2.png?raw=true)

I removed the sales data of each month and grouped the total sales by UPC number.

![3](https://github.com/LeonDosovitsky/Images/blob/main/Images/excel_3.png?raw=true)

I made a Left Join to add the product data to the sales table.

![4](https://github.com/LeonDosovitsky/Images/blob/main/Images/excel_4.png?raw=true)

I loaded to table into Excel and added the quartile function with an IF statement to return the rows that are in the first quartile as TRUE.
To finish, I sorted the data to only show the TRUE.

![5](https://github.com/LeonDosovitsky/Images/blob/main/Images/excel_5.png?raw=true)

For the stores analysis I copied the Power Query steps for UPC's and made a new query.
I changed the Group by to use the store ID instead of the UPC number.

![6](https://github.com/LeonDosovitsky/Images/blob/main/Images/excel_6.png?raw=true)

I loaded to table into Excel and added the quartile function with an IF statement to return the rows that are in the first quartile as TRUE.
To finish, I sorted the data to only show the TRUE.

![7](https://github.com/LeonDosovitsky/Images/blob/main/Images/excel_7.png?raw=true)

# SQL

## Coca Cola products :
I loaded my tables into SSMS and created the following CTE's :
- Combines all the sales into 1 column
- Groups sales by UPC
- Separates the UPC's in 4 quartiles

![8](https://github.com/LeonDosovitsky/Images/blob/main/Images/SQL_UPC.png?raw=true)

I joined a list of all the products and returned the product information for ones in the first quartile.


## Stores :
Loaded my tables into SSMS and created the following CTE's :
- Combines all the sales into 1 column
- Groups sales by store
- Separates the stores in 4 quartiles

![9](https://github.com/LeonDosovitsky/Images/blob/main/Images/SQL_store.png?raw=true)

Returned the store ID for the stores in the first quartile.

# Python

## Coca Cola products :

- Merged the product information to the sales data
- Combined all sales into 1 column
- Grouped the sales by UPC number
- Created 4 buckets based on total sales
- Returned the product information for the items in the first quartile

![10](https://github.com/LeonDosovitsky/Images/blob/main/Images/python_UPC.png?raw=true)
<br><br><br>

## Stores :
- Combined all sales into 1 column
- Grouped the sales by store ID
- Created 4 buckets based on total sales
- Returned the store ID's for the ones in the first quartile

![11](https://github.com/LeonDosovitsky/Images/blob/main/Images/python_store.png?raw=true)
