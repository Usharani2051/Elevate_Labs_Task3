# Elevate_Labs_Task3

**Sales & Profit Trends Dashboard – Power BI**

This repository contains a Power BI Sales & Profit Dashboard designed to analyze and visualize key business metrics for data-driven decision-making.

**About the Project**

The Sales & Profit Trends Dashboard provides an interactive view of sales performance, profitability, and regional distribution over the period 2018–2021.
It enables dynamic exploration of data to identify top-performing categories, track seasonal sales trends, and uncover opportunities for margin improvement.

**Features & KPIs**

 - Total Sales: $284.58K
 - Total Profit: $28.29K
 - Orders: 570
 - Sales Growth: 29.65%
 - Profit Margin: 9.94%
 - Average Monthly Profit: $2.36K
 - Regional performance via map & profit breakdown
 - Top categories & sub-categories by sales and profit
 - Seasonal and monthly profit trends

**Data Visualizations**

Chart Title	                              Description
Sales Trend Over                          Time	Line chart showing monthly sales growth and seasonal peaks (Sep 2018, Aug 2020).
Sales by Category & Sub-Category	        Bar charts highlighting top revenue drivers and underperforming products.
Regional Sales & Profit	                  Map and bar chart visualizing sales distribution and profit margins across regions.
Profit Trend by Month	                    Line chart showing monthly profit fluctuations with peak and low months.
Sales vs Profit	                          Combo chart comparing revenue against profit levels over time.

**Tools Used**

 - Power BI Desktop – Data modeling, DAX measures, and visualization
 - Excel / CSV Data – Source dataset: sales_and_profit_trends.csv

 - DAX Measures for KPIs:

   DAX
    - Total Sales = SUM('SalesAndProfitTrends'[Sales])
    - Total Profit = SUM('SalesAndProfitTrends'[Profit])
    - Profit Margin = DIVIDE([Total Profit], [Total Sales], 0)
    - Orders = DISTINCTCOUNT('SalesAndProfitTrends'[OrderID])
    - Sales Growth % = 
      VAR PrevSales = CALCULATE([Total Sales], DATEADD('SalesAndProfitTrends'[OrderDate], -1, YEAR))
      RETURN DIVIDE([Total Sales] - PrevSales, PrevSales, 0)

**Key Insights**

 - Technology is the top revenue-generating category, followed by Furniture and Office Supplies.
 - West region leads in both sales ($81.02K) and profit (45% of total profit).
 - Seasonal peaks in Sep 2018 and Aug 2020; lowest profits in April, Aug, Sep.
 - Opportunities in Central and South regions to improve margins.
 - Underperforming sub-categories like Binders and Supplies present growth potential.


PowerBI project link: https://app.powerbi.com/links/7K6cvR8Ksd?ctid=46805c18-2ee4-4b75-970e-c9ce28de3cbf&pbi_source=linkShare




