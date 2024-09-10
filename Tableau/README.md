# Tableau Story - AdventureWorks Data Warehouse (2022)

![image](https://github.com/user-attachments/assets/b29fe78e-7819-49b4-9e3b-9dcd62d95a4a)


## Table of Contents
1. [Overview](#overview)
2. [Key Steps](#key-steps)
   - [Data Extraction](#data-extraction)
   - [Data Modeling](#data-modeling)
   - [Dashboard Creation](#dashboard-creation)
   - [Tableau Story](#tableau-story)
3. [How to Use the Story](#how-to-use-the-story)
4. [To-do](#to-do)

## Overview

This project showcases a Tableau Story built using the **AdventureWorks Data Warehouse (2022 version)** dataset. The story provides insights into various aspects of the business, such as Overall Market Performance, a deeper look into Customers, Currency, Products and Promotions, each represented by a dashboard displaying information about each aspect.

The project follows the steps from exporting data from **SQL Server**, creating a basic Snowflake schema data model in Tableau, and constructing several interactive dashboards. These dashboards are presented as a **Tableau Story** for better navigation and reporting.

## Key Steps

### Data Extraction
- The dataset used is the <a href = "https://learn.microsoft.com/en-us/sql/samples/adventureworks-install-configure?view=sql-server-ver15&tabs=ssms">**AdventureWorks Data Warehouse (2022 version)**.</a>
- The .bak file (attached in the link above) was restored in SQL Server and after validating the data restored, the relevant and important data was then exported to an Excel file.
- The extracted Excel files contain tables such as `FactInternetSales`, `DimCustomer`, `DimProduct`, and `DimSalesTerritory`.

### Data Modeling
- In Tableau, the **Data Source** tab was used to establish a simple **snowflake schema** model.
- Handled issues concerning Data Validation, Handling NULL Values and casting the columns into the correct data type to facilitate the process of creating relationships between the model.
- The **FactInternetSales** table was used as the central fact table, and dimensions such as `DimCustomer`, `DimProduct`, and `DimSalesTerritory` were linked via appropriate keys to create a simple yet effective data model.

![image](https://github.com/user-attachments/assets/186ba883-37a8-48f1-a0a4-a9e4e1665717)


### Dashboard Creation
- Several dashboards were built to display different insights, including:
  - **Overall Market Analysis**: A General view about the performance of the organization such as sales, growth over time.
  - **Customer Demographics**: Analyzing customer segmentation by different segments such as age, region, number of children and more.
  - **Product Analysis**: Highlighting the performance of categories.
  - **Currency Analysis**: A deeper view into the revenue generated and the currencies used.
  - **Promotion Analysis**: Looking into how promotions impact sales and how different sales are during the promotions lifetime.

### Tableau Story
- The individual dashboards were compiled into a **Tableau Story** for cohesive storytelling.
- Users can navigate through different sections of the report to get a complete picture of the business insights.

## How to Use the Story

1. **Explore the Story using Tableau Public**: The story, dashboard and sheets used to create the dashboards can be accessed and explored interactively <a href ="https://public.tableau.com/app/profile/ahmed.metwaly6299/viz/TaskDay2/Story1_1">**here**</a>
   
## To-do
- Improve the dashboard by creating more charts, making the current dashboard more spacious, adjusting the tooltips for more interactivity and facilitaing the process of drilling down
- Creating a Presentation to simulate a scenario where this dashboard would be shown to management.

