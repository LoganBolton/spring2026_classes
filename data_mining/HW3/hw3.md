# Q1
1. What is a Data Warehouse? Please list 3 kind of applications of the Data Warehouse method

A datawarehouse is a centralized collection of data from various sources. It can be used for things like creating dashboards that describe the current state of a business, analyzing the behaviors of customers or forceasting future trends of what the business related data could look like.

2. List and explain 3 schemas of data Warehouses.

The three types are star schema, snowflake schema, and fact constellation. A star schema has one fact table connected to dimension tables. A snowflake schema is a more normalized version with smaller dimension tables. A fact constellation schema has multiple fact tables that share dimension tables.

# Q2

1. List and explain at least 4 typical OLAP operations.

Some typical OLAP operations would be things like summarizing data, looking at more detailed data, focusing on one category, and comparing data across multiple conditions. For example, this could mean looking at total sales by year, then breaking it down by month, viewing data for only one region or customer group, or comparing sales for certain products in specific places and time periods.

2. How many cuboids are there in a 3-dimensional cube with 2,4 and 5 levels on its first, second and third dimension correspondingly?

(2 + 1)(4 + 1)(5 + 1) 
= 3 × 5 × 6 
= 90

There would be 90 cuboids total across each dimension.

3. Index the following table on the animal type column with Bitmap index method.

4. What are the drawbacks of the Bitmap index method?

# Q3

Suppose that a data warehouse consists of the three dimensions: time, doctor, and patient, and the two measures: count and charge, where charge is the fee that a doctor charges a patient for a visit.

1.  Draw a schema diagram for the above data warehouse using a schema of your choice. You must name your choice.