# Microsoft SQL Business Intelligence Tasks

![image](https://github.com/user-attachments/assets/f30c1852-4121-4a13-bcef-ff2dd39f583f)

This repository contains various Business Intelligence (BI) and Extract, Transform, Load (ETL) tasks using SQL Server Integration Services (SSIS), SQL Server Reporting Services (SSRS), and Cube design using SQL Server Analytics Services. The tasks are based on exercises and labs provided in the documents attached.

## Table of Contents

- [Prerequisites](#prerequisites)
- [SSIS](#ssis)
- [SSAS](#ssas)
- [SSRS](#ssrs)
- [Accessing The Tasks](#accessing-the-tasks)
- [Summary](#summary)
---
## Prerequisites
1. **SQL Server 2022**
2. **SQL Server Management Studio 20**
3. **Visual Studio Community Edition**
4. **SQL Server Integration, Analysis, Reporting Services**

Start by restoring the relevant Databases into SQL Server, Make sure the services are running and fully functional before you can access the packages (NOTE: You might have to adjust connection settings to your own settings)
---
## SSIS

This section involves creating and managing SSIS packages for data transfer, transformation, and backups.

### Key Tasks:
1. **Transfer Department Data**  
   - Design an SSIS package using the wizard to transfer Department data from the `ITI` database to the `Test` database.
   - Before transferring, truncate the Department table in the `Test` database.

2. **Transfer Student Data to Delimited File**  
   - Use the wizard to transfer Student data (St_id, St_Fname, St_Lname, St_address) from the `ITI` database to a new delimited file named `Student.txt`.
   - Ensure the first row contains the column names.

3. **Student Data Transfer with Transformation**  
   - Create an SSIS package to transfer Student data from the `ITI` to the `Test` database.
   - If the Student table exists, delete all data using the `Execute SQL Task`.
   - Merge the first and last names into one field (Full Name) using the `Derived Column` component.
   - Set up error handling to display a message box if an error occurs.

4. **Course Data Split and Merge**  
   - Design an SSIS package to split Course data from the `ITI` database into three separate files based on course duration (<30, =30, >30 hours).
   - Merge two of the files using the `Merge` and `Union` components.
   
5. **Database Backup**  
   - Perform a full backup of the `Test` database.

---

## SSAS

This section focuses on creating and managing OLAP cubes to analyze sales data using SQL Server Analysis Services (SSAS).

### Key Tasks:
1. **Product Cube**  
   - Create a cube named `Product Cube` that shows product quantity over the years.
   - Use the Product dimension to display columns like Product ID and Product Name, and the Time dimension to display the Calendar Year.
   - Use the fact table [Fact Sales] to show the quantity measure.

2. **Product-Customer Cube**  
   - Create a cube named `Prod_Cust Cube` to show the relationship between products and customers over time.
   - Include dimensions like Product ID, Product Name, Product Category, and Customer Name.
   - Create a calculated measure "Sales Unit Price" using the expression `[Qty Total Price] / [Qty]`.
   - Set up a KPI to ensure the quantity sold is at least 1,000 units, and create Arabic translations for the dimensions and measures.

3. **Sales Cube**  
   - Create a cube named `Sales Cube` to show all data in the SalesDW database.
   - Include measures like Customer Count, Product Count, Qty, Total Price, and Number of Orders.
   - Set up a perspective called `Channel Product Perspective` to display data related to customers, channels, and total sales.

4. **Pivot Table & Chart**  
   - Use Microsoft Excel to create pivot tables and charts based on the cubes created.

---

## SSRS

This section focuses on creating reports using SQL Server Reporting Services (SSRS) to visualize student and sales data.

### Key Tasks:
1. **Tabular Student Report**  
   - Create a tabular report using a wizard to display student data.
   - Add a header with a logo and a footer showing the username and execution time.
   - Add conditional formatting to highlight students older than 23, and display the full name using expressions.

2. **Matrix Report (Sales Data)**  
   - Create a matrix report that displays the sum of quantity sold per Product ID and Salesman Name, based on a sample sales table.

3. **Chart Report**  
   - Create a chart to visualize the sales quantity data per Product ID and Salesman Name.

4. **Grade Indicator Report**  
   - Design a report that displays student grades with indicators:
     - Grades 0-50: Red
     - Grades 51-60: Yellow
     - Grades 61-100: Green

5. **Stored Procedure Reports**  
   - Create reports that display data from stored procedures, including filtering students by age and allowing parameter selection for department IDs.

6. **Linked Reports & Data from Cube**  
   - Generate linked reports and display data from an OLAP cube, filtering by year.
   
---
## Accessing The Tasks
The tasks can be made accessible by cloning this repository to your local machine
```bash
git clone https://github.com/AhmedMetwaly1287/SQLBI.git
```
---

## Summary

This repository showcases a variety of ETL and BI tasks, demonstrating skills in SSIS, SSAS, and SSRS, as well as integrating data from different sources and creating insightful reports and dashboards. 
Each lab focuses on different aspects of data processing and analysis, with detailed instructions for building efficient solutions.
