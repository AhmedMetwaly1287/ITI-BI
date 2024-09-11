# Microsoft PowerBI - AdventureWorks Dashboard

![image](https://github.com/user-attachments/assets/3105ffe3-18ef-4ef5-ad7b-fa69d0ccd7fa)

## Table of Contents
1. [Overview](#overview)
2. [Key Steps](#key-steps)
   - [Data Ingestion & Transformation](#data-ingestion--transformation)
   - [Data Modeling & Creating New Measures](#data-modeling--creating-new-measures)
   - [Dashboard Creation](#dashboard-creation)
3. [How to access the Dashboard](#how-to-access-the-dashboard)
4. [To-do](#to-do)

## Overview

This project showcases a Microsoft PowerBI Dashboard built using the **AdventureWorks Database (2022 version)** dataset. The dashboard provides insights into various aspects of the business, such as Overall Market Performance, identifying important KPIs such as Number of Orders, Total Due, Number of Shipped Orders, Due Orders and Orders placed alongsides other crucial information for the organization.

The project follows the steps from restoring the data into **SQL Server**, Ingesting it into PowerBI, Performing basic transformations using Power Query, creating a basic Star schema data model in PowerBi, and constructing several interactive dashboards.

## Key Steps

### Data Ingestion & Transformation
- The dataset used is the <a href = "https://learn.microsoft.com/en-us/sql/samples/adventureworks-install-configure?view=sql-server-ver15&tabs=ssms">**AdventureWorks Database (2022 version)**.</a>
- The .bak file (attached in the link above) was restored in SQL Server.
- Microsoft PowerBI then connected directly to SQL Server in order to ingest the relevant tables and functions needed.
- Power Query was then leveraged to perform transformations to the data at hand such as handling NULL values, casting columns into the correct Data Type, getting rid of duplicate values to enforce uniquness in Dimensions, Merging queries with each other and then expanding the merged queries in one query.

### Data Modeling & Creating New Measures
- In PowerBI, the **Model View** tab was used to establish a simple **Star Schema** model, `Sales Order` being the fact table and the surronding tables being the Dimension Tables.
- Handled issues concerning Data Validation, Handling NULL Values and casting the columns into the correct data type to facilitate the process of creating relationships between the model, created multiple relationships between the Date Dimension and Fact Table and leveraged `USE RELATIONSHIP` in PowerBI to be able to use the relationships each individually.
- The `ufnGetSalesOrderStatusText` function was used to create the **Status** Table to identify the status of the order.
- Creating new measures using DAX Functions such as `Total of Tax` and `Correct Total Tax` to compare between the error values and the correct values and use the correct ones in the visualization process.
- Merged between queries such as `Sales Order` and `Sales Order Detail`.

![image](https://github.com/user-attachments/assets/665c431f-a1f2-4fc3-b0c0-5216bcce344b)


### Dashboard Creation
- Several dashboards were built to display different insights.
- Used Bookmarks to Facilitate navigation between Dashboard Pages.
- Created a tooltip as an example to make the process of drilling down easier.


## How to access the Dashboard

1. **A General Overview of the Dashboard**: The Dashboard can be viewed in a PDF form by clicking <a href="https://drive.google.com/file/d/1vqmuYXsoBuodRBOyjziEIzm0_zJ71pTo/view?usp=sharing">here</a>!
2. **Access the Entire Dashboard**: You can access and explore the Dashboard interactively by downloading this Folder and accessing the **Task.pbix** in this Folder.
   
## To-do
- Improve the dashboard by creating more charts, making the current dashboard more spacious, adjusting the tooltips for more interactivity and facilitaing the process of drilling down
- Creating a Presentation to simulate a scenario where this dashboard would be shown to management.


