# Corporate KPI Dashboard

![Corporate KPI](https://github.com/user-attachments/assets/13c9cd59-30d6-4b05-ac76-2a1de40f4638)


## Problem Statement

This dashboard provides the heads of Singapore SportsHub with comprehensive insights into event metrics, including the number of events, attendance figures, total footfall, and EBITDA for their various venues on a monthly and year-to-date basis. It enables SportsHub to assess the performance of each venue while offering a quick overview of upcoming events, ticket sales, and venue capacities. The summary page highlights SportsHub's profitability and identifies areas for improvement.


### Steps followed 

- Step 1: Load data into Power BI Desktop from various sources. The footfall and event data were sourced from Azure Synapse DB, while financial data was retrieved from monthly Excel files stored in a shared folder managed by the Finance Team for enhanced data security.

- Step 2: Open the Power Query Editor to append all monthly finance files into a single consolidated file for reporting purposes.

- Step 3: In the Model View, establish a data model by connecting the various tables based on common keys. Additionally, create a Date table utilizing time intelligence functions.

- Step 4: In the Report View, select a theme under the View tab to maintain visual consistency across the dashboard.

- Step 5: Create separate pages within the report for a summary and detailed analysis of footfall, events, and financial KPIs.

- Step 6: Add visual filters (slicers) for "Year" and "Month" to the left pane of each page, allowing users to filter data interactively.

- Step 7: On the Summary Page, incorporate two card visuals for each KPI — one displaying monthly figures and the other showing year-to-date (YTD) values (e.g., Monthly Footfall and YTD Footfall).

- Step 8: Create measures and calculated columns for Monthly and YTD KPIs. For instance, the following DAX expression was written to generate a new column:
       
        Footfall YTD = TOTALYTD(Sum(Footfall[Footfall]), 'Date'[Date])


![Footfall YTD](https://github.com/user-attachments/assets/4de6124e-3a2e-4f67-9b96-e8415db1826d)


 - Step 9: Repeat similar steps to create measures for the remaining KPIs, ensuring consistency and accuracy across all calculations.

 - Step 10: Publish the completed report to Power BI Service for distribution and accessibility to stakeholders.
 

# Snapshot of Dashboard

 - KPI Summary Page
   
![Corporate KPI Dashboard - Summary](https://github.com/user-attachments/assets/4a8cc57a-eceb-40c4-a99b-9e4849cb8a59)

 - Footfall Page
   
 ![Corporate KPI Dashboard - Footfall](https://github.com/user-attachments/assets/bfde390f-e2f9-4e51-b222-971de1f14cfa)

 - Event Attendance Page
   
 ![Corporate KPI Dashboard - Event Attendance](https://github.com/user-attachments/assets/072beac3-8107-4669-8752-cd10395fd3cb)

 - Finance Page
   
 ![Corporate KPI Dashboard - Finance](https://github.com/user-attachments/assets/6261c422-be9e-4659-88e7-5763b8911418)

 

# Data Model

![Corporate KPI Dashboard - Data Model](https://github.com/user-attachments/assets/9e140596-11cd-40da-b81b-d6217e000c49)
