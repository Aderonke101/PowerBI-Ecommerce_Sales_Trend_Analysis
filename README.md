## E-commerce Sales Dashboard

## Overview

This project showcases an interactive E-commerce Sales Dashboard created using Power BI. It provides insights into key metrics like YTD Sales, YTD Profit, YTD Quantity, and YTD Profit Margin. Additionally, it visualizes sales performance across various categories, regions, states, shipping types, and top/bottom-performing products.

## Tools Used

Microsoft Excel: For data cleaning and removing duplicates.

Microsoft PowerPoint: For designing the custom dashboard background.

Microsoft SQL Server (MSSQL): For data storage and querying.

Power BI: For creating the dashboard and connecting datasets.


## Project Workflow

1. Data Cleaning:

Removed duplicates and unnecessary data entries using Excel.

Ensured the data was clean and ready for analysis.



2. Database Setup:

Loaded the cleaned data into MSSQL.

The data consisted of two related tables.



3. Power BI Setup:

Imported the tables from MSSQL into Power BI.

Created a new Calendar Table for better time intelligence analysis.

Established relationships between the tables.



4. Dashboard Development:

Designed a visually appealing dashboard background using PowerPoint.

## Created new measures for key metrics and visualizations:

YTD Sales

YTD Profit

YTD Quantity

YTD Profit Margin


## Built custom charts, graphs, and maps:

Sales by Category

Sales by Region

Sales by State

Top 5 Products by YTD Sales

Bottom 5 Products by YTD Sales

YTD Sales by Shipping Type


Applied formatting to ensure consistency and readability.

5. Sales by Location (Map): Used "US_longitude_latitude_codes" for geospatial mapping, visualizing sales across different regions using geographic coordinates.


6. Measures and DAX Code:

All metrics and calculations (e.g., YTD measures, profit margin) were created using DAX (Data Analysis Expressions). The code for these measures is documented in the project files.



6. Screenshot:

A screenshot of the completed dashboard is included in the repository.
!![Ecommerce Dashboard](Ecommerce%20Sales%20Dashboard_Screenshot.png)
## Features

Dynamic Metrics: Automatically updates based on selected filters (e.g., Consumer, Corporate, Home Office components).

Interactive Visualizations: Offers a user-friendly experience to explore data trends and insights.

Custom Design: Unique dashboard layout created using PowerPoint.


## Repository Contents

Ecommerce_Sales_Dashboard.pbix: The Power BI dashboard file.

Ecommerce_Cleaned-Data.csv: The cleaned data used in the project.

Ecommerce_(Map)-Data.csv: The Cleaned data that was used for the Map in the dashboard. The data contain The United States Longititude and Latitude Codes. The Country name and Abbreviations.

Dashboard_Background.pptx: The PowerPoint file used for the background design.

DAX_Measures(read-me).md: A file containing all DAX measures notes and the Full meaning of all abbreviations used. 

DAX_Measures-Formula: A file containing all DAX measures Formulas used in the project

Screenshots/: Folder containing screenshots of the dashboard.


## How to Use

1. Clone this repository:

git clone <repository_url>

2. Open the Ecommerce_Sales_Dashboard.pbix file in Power BI Desktop.

3. Connect to your local MSSQL server and load the data if needed.

4. Explore the dashboard interactively or modify it to suit your needs.



## Acknowledgments

Special thanks to the following tools and platforms:

Power BI Community for resources and tutorials.

Microsoft Office Suite for Excel and PowerPoint.

Microsoft (SQL Server management Studio(SSMS))

