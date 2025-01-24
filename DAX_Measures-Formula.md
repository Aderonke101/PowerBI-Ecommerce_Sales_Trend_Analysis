# Dax Formulas for E-Commerce Dashboard

## Overview

The DAX (Data Analysis Expressions) formulas in this project are designed to calculate key business metrics such as sales, quantities, and profits over various time periods. These formulas enable the creation of dynamic reports and dashboards, allowing users to track performance across different dimensions, such as Year-to-Date (YTD), Previous Year-to-Date (PTYD), Year-over-Year (YoY), and Profit Margins. 

The DAX formulas also include measures that apply visual indicators (icons and colors) to represent performance trends, making it easier to interpret the data.

The formulas are structured to capture essential KPIs, like total sales, quantity sold, and profit, and compare them across time periods. By incorporating these calculations, users can assess business performance, detect trends, and identify areas that need attention, all in real-time.



# DAX Measures

## Measures for Sales Table
1. YTD Sales = TOTALYTD(SUM(ecommerce_data[sales_per_order]), 'Calendar'[Date])

2. YoY Sales = ([YTD Sales]- [PYTD Sales])/ [PYTD Sales]

3. PYTD Sales = CALCULATE(SUM(ecommerce_data[sales_per_order]), DATESYTD(SAMEPERIODLASTYEAR('Calendar'[Date])))

4. Sales Icon colour = IF([YoY Sales]>0, "Green", "Red")

5. Trend = VAR positive_icon = UNICHAR(9650)
             VAR negative_icon = UNICHAR(9660)
             VAR result = IF([YoY Sales]>0, positive_icon, negative_icon)
             return result


## Measures for Quantity Table
1. YTD Qty = TOTALYTD(SUM(ecommerce_data[order_quantity]), 'Calendar'[Date])

2. YTD Concatenated Qty = CONCATENATE("#", FORMAT([YTD Qty]/1000, "0.0k"))

3. YoY QTY = ([YTD QTY]- [PYTD Qty])/ [PYTD Qty]

4. PYTD Qty = CALCULATE(SUM(ecommerce_data[order_quantity]), DATESYTD(SAMEPERIODLASTYEAR('Calendar'[Date])))

5. Qty Icon colour = IF([YoY QTY]>0, "Green", "Red")

6. Qty Icon = VAR positive_icon = UNICHAR(9650)
             VAR negative_icon = UNICHAR(9660)
             VAR result = IF([YoY QTY]>0, positive_icon, negative_icon)
             return result

## Measures for Profit Table
1. YTD Profit = TOTALYTD(SUM(ecommerce_data[profit_per_order]), 'Calendar'[Date])

2. YoY Profit = ([YTD Profit]- [PYTD Profit])/ [PYTD Profit]

3. PYTD Profit = CALCULATE(SUM(ecommerce_data[profit_per_order]), DATESYTD(SAMEPERIODLASTYEAR('Calendar'[Date])))

4. Profit Icon colour = IF([YoY Profit]>0, "Green", "Red")

5. Profit Icon = VAR positive_icon = UNICHAR(9650)
             VAR negative_icon = UNICHAR(9660)
             VAR result = IF([YoY Profit]>0, positive_icon, negative_icon)
             return result

## Measures for Profit Margin Table
1. Profit Margin = SUM(ecommerce_data[profit_per_order])/ SUM(ecommerce_data[sales_per_order])

2. YTD Profit Margin = TOTALYTD([Profit Margin], 'Calendar'[Date])

3. YoY Profit Margin = ([YTD Profit Margin]- [PYTD Profit Margin])/ [PYTD Profit Margin]

4. PYTD Profit Margin = CALCULATE([Profit Margin], DATESYTD(SAMEPERIODLASTYEAR('Calendar'[Date])))

5. Profit margin Icon colour = IF([YoY Profit Margin]>0, "Green", "Red")

6. Profit Margin Icon = VAR positive_icon = UNICHAR(9650)
             VAR negative_icon = UNICHAR(9660)
             VAR result = IF([YoY Profit Margin]>0, positive_icon, negative_icon)
             return result


## Conclusion

The DAX formulas implemented in this project provide a robust set of tools for performing detailed data analysis. They support dynamic reporting and visualizations in Power BI, facilitating efficient business decision-making. With these formulas, businesses can track key metrics such as sales growth, quantity sold, and profit margins while gaining actionable insights through comparative metrics like YoY and YTD analysis.

By leveraging these formulas, users can create interactive and informative dashboards that visually highlight key trends and performance indicators, driving better business insights and actions.
