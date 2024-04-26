It’s become well known that in today’s world, data is one of the most important things in our 
day-to-day lives. From data alone, we can learn a human’s entire life and predict their future. However, 
such data comes in a raw form that doesn’t help provide any insights, and that’s where we come in. We 
have to clean the data and organize it in order to come up with an understandable insight that could 
help further improve the business, and the business we’re doing the data for is a restaurant. 
Here we’re tasked with a plan to design and implement a dimensional model for storing menu 
items, customer orders, inventory, employee information, and sales data. Menu Items Dimension stores 
details about the menu items offered by the restaurant. Inventory Dimension stores details about 
inventory items such as item ID, name, quantity in stock, supplier information, etc. Employee Dimension
contains information about employees such as employee ID, name, work duration, etc. Sales Fact Table 
captures transactional data related to sales. It typically includes foreign keys referencing the dimension 
tables, as well as measures such as quantity sold, total sales amount, discounts applied, timestamps, etc. 
This table serves as the central hub for analyzing sales data. Order Dimension Depending on the 
complexity of the system, you might create a separate dimension table for orders. This table could 
contain attributes like order ID, order date, payment method, etc. Date Dimension, If time-based 
analysis is important, a time dimension table can be included with attributes such as date, day of the 
week, month, quarter, year, etc.
Establish relationships between the fact table and dimension tables using foreign keys. For 
example, the sales fact table would have foreign keys referencing the menu items, employees involved 
in the sale, etc. Define the level of granularity for the fact table. In this case, it could be at the level of 
individual sales transactions, capturing details of each sale. Consider creating aggregated tables for 
faster querying and reporting. Aggregations can be based on different dimensions and measures, such 
as total sales by item, total sales by customer, etc.
To implement the features we need in this project, we can use toad to write PL/SQL code for 
inventory management, to track stock levels and ingredient usage. *-The way we implemented it-*
We implemented SQL queries designed to analyze monthly sales data to gain insights into sales 
performance, including sales velocity, transaction count, and sales growth. We implemented another 
query that provides a breakdown of sales by order type for each month, aiding in understanding the 
distribution of sales across different types of orders over time. Another one that helps in identifying 
peak hours for morning and night shifts each month, enabling effective scheduling and resource 
management. A query that identifies items that have been purchased only once. It calculates the total 
quantity of each item and filters items with a total quantity of 1. The result includes the item name, 
category, price, and the number of stocks. It's sorted by category. A query that calculates the growth of 
selling products over time. It aggregates the total sales quantity for each month and calculates the 
previous year's sales amount. The difference between the current year's sales and the previous year's 
sales gives the sales growth for each month. A query that helps our business identify products that 
perform poorly each month, enabling us to adjust inventory, marketing strategies, or even consider 
discontinuing such products to optimize business performance. A query that presents the sales of each 
category. It calculates the total quantity, total price, and sales revenue for each category. Additionally, it 
computes the percentage rank of sales revenue among all categories. A query that identifies the most 
3
selling meal in each category. It ranks meals based on their total sales within each category and selects 
the meal with the highest sales in each category. A query that provides the most selling meal in each 
category along with its revenue. It calculates the total revenue for each meal by subtracting the total 
ingredient cost from its total sales. The results are grouped by meal name, category, total sales, total 
ingredient cost, and revenue.
