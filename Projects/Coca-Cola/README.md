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

<img width="1919" height="1014" alt="Image" src="https://github.com/user-attachments/assets/6369dafa-e24c-49b2-8dd6-12a909591f1c" />

I added a Total Sales column that calculates the sum of all sales.

<img width="1418" height="704" alt="Image" src="https://github.com/user-attachments/assets/3ac387de-95a0-4c33-b48e-ef37ccd6ecba" />

I removed the sales data of each month and grouped the total sales by UPC number.

<img width="1133" height="758" alt="Image" src="https://github.com/user-attachments/assets/8196e193-bac5-41f2-b398-ffadedddc9fc" />

I made a Left Join to add the product data to the sales table.

<img width="695" height="625" alt="Image" src="https://github.com/user-attachments/assets/ea79e4c1-2817-4258-a076-a88b6ea86b7c" />

I loaded to table into Excel and added the quartile function with an IF statement to return the rows that are in the first quartile as TRUE.
To finish, I sorted the data to only show the TRUE.

<img width="1913" height="1027" alt="Image" src="https://github.com/user-attachments/assets/0408bc9b-161a-4409-80b9-358735851e54" />

For the stores analysis I copied the Power Query steps for UPC's and made a new query.
I changed the Group by to use the store ID instead of the UPC number.

<img width="1240" height="644" alt="Image" src="https://github.com/user-attachments/assets/09d6aa60-5739-4b6c-9a9d-c8128c3fd74f" />

I loaded to table into Excel and added the quartile function with an IF statement to return the rows that are in the first quartile as TRUE.
To finish, I sorted the data to only show the TRUE.

<img width="1919" height="1010" alt="Image" src="https://github.com/user-attachments/assets/0224d645-d7df-41a4-bff6-7eca4b68b374" />

# SQL

## Coca Cola products :
I loaded my tables into SSMS and created the following CTE's :
- Combines all the sales into 1 column
- Groups sales by UPC
- Separates the UPC's in 4 quartiles

<img width="1918" height="1032" alt="Image" src="https://github.com/user-attachments/assets/24613964-f35f-4d60-b2c3-5358043bbe23" />

I joined a list of all the products and returned the product information for ones in the first quartile.


## Stores :
Loaded my tables into SSMS and created the following CTE's :
- Combines all the sales into 1 column
- Groups sales by store
- Separates the stores in 4 quartiles

<img width="1917" height="1031" alt="Image" src="https://github.com/user-attachments/assets/eb77f019-fb2f-44dc-bfdf-261739025374" />

Returned the store ID for the stores in the first quartile.

# Python

## Coca Cola products :

- Merged the product information to the sales data
- Combined all sales into 1 column
- Grouped the sales by UPC number
- Created 4 buckets based on total sales
- Returned the product information for the items in the first quartile

<img width="1210" height="708" alt="Image" src="https://github.com/user-attachments/assets/7864f3f8-aa31-4b8c-a4e4-eecc5a922be2" />
<br><br><br>

## Stores :
- Combined all sales into 1 column
- Grouped the sales by store ID
- Created 4 buckets based on total sales
- Returned the store ID's for the ones in the first quartile

<img width="1204" height="775" alt="Image" src="https://github.com/user-attachments/assets/b3da29de-0cd6-423e-b9e7-5c74ee4e9ad8" />
