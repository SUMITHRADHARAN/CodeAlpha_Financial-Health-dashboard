# CodeAlpha_Financial-Health-dashboard
A Power BI dashboard for SMEs analyzing financial health. Features include visualizing income statements, balance sheets, and cash flow; analyzing profitability trends; and forecasting for planning using the Microsoft Financial Sample data.

This README provides step-by-step guidance on setting up and using the Financial Health Dashboard, a Power BI solution designed to help SMEs analyze their financial status with real-time insights, budgeting tools, and forecasting capabilities.
Financial Health Dashboard: Step-by-Step Guide

1. Project Objective and Requirements
Objective:
Develop an interactive Power BI dashboard that provides a comprehensive analysis of an organization's financial status, tailored for Small and Medium Enterprises (SMEs).
Key Requirements:
Visualize income statements, balance sheets, and cash flows.
Analyze profitability trends over time.
Provide forecasting for budgeting and financial planning.
Deliverable:
An interactive Power BI .pbix report file with dynamic visualizations and actionable insights.

3. Getting Started: Prerequisites
Before you begin, ensure you have the necessary software and data:
Software: Download and install Power BI Desktop (free).
Dataset: This project uses the Microsoft Financial Sample Excel workbook as the foundational data source. Download and save this Excel file locally.

4. Step-by-Step Setup Instructions
Follow these steps to load the data and build the core report structure:
Step 3.1: Load the Data into Power BI Desktop
Open Power BI Desktop.
On the Home ribbon, click Get data > Excel workbook.
Select the financial-sample.xlsx file you downloaded.
In the Navigator window, select the financials table and click Load.
Step 3.2: Transform Data (Power Query Editor)
You can clean the data slightly using the Power Query Editor:
Click Transform data on the Home ribbon (if you didn't do it during the load, go to Home > Edit queries).
Ensure all columns have the correct data types (e.g., Date, Currency, Decimal Number).
Close & Apply changes.
Step 3.3: Create Key Performance Indicators (KPIs)
Create core measures using Data Analysis Expressions (DAX) to enable analysis:
In the Fields pane, right-click the financials table and select New measure.
Create measures for:
Total Revenue: Total Revenue = SUM(financials[ Sales ])
Total Profit: Total Profit = SUM(financials[Profit])
Gross Margin %: Gross Margin % = DIVIDE([Total Profit], [Total Revenue])
Step 3.4: Visualize Profitability Trends
Create the first report page focusing on profitability over time:
Page Title: Add a text box labeled "Profitability Analysis".
Line Chart: Drag a Line chart visual onto the canvas.
X-axis: Drag the Date field (grouped by Month or Year).
Y-axis: Drag Total Revenue and Total Profit measures.
Slicer: Add a Slicer visual and use the Year field to filter the data interactively.

Step 3.5: Build Financial Statement Structure (Matrix Visual)
Use the Matrix visual to create a structured layout mimicking an income statement:
New Page: Create a new report page labeled "Income Statement".
Matrix Visual: Drag a Matrix visual onto the canvas.
Rows: Use the Product or Segment columns to categorize line items (for a simple P&L approximation with the sample data).
Columns: Use the Month Name field.
Values: Use the Total Revenue, COGS, and Total Profit measures.
Waterfall Chart: Add a Waterfall Chart next to the matrix to visually show the flow from total revenue down to total profit, using Segment as the category breakdown.

Step 3.6: Implement Forecasting
Use Power BI's built-in analytics feature for a quick revenue forecast:
Go back to your profitability page.
Select the Line Chart you created in Step 3.4.
In the Visualizations pane, click the Analytics icon (the magnifying glass).
Expand the Forecast section and click Add.
Configure the forecast (e.g., Forecast points: 12, Seasonality: 12 for monthly data). This will add a projection line to your chart.

6. Usage and Interactivity
The final report should be fully interactive. Users can leverage the slicers to filter data by region or time period, hover over visuals for specific details, and use the different report tabs to switch between profitability trends, detailed statements, and forecasts.

Conclusion:
The Power BI Financial Health Dashboard provides a robust, interactive solution for SMEs to monitor and analyze their financial performance using real-time insights, core financial statement visualization (income statement, balance sheet, cash flows), profitability trends, and built-in forecasting capabilities.
By following the provided steps using the Microsoft Financial Sample Excel workbook, users can create a powerful, dynamic tool to inform strategic decision-making and enhance financial planning within their organizations.


