# Sales & Customer Dashboards

An interactive Tableau dashboard analyzing sales performance and customer behavior, 
with year-over-year comparisons driven by a dynamic year parameter.

## Overview
This project provides a business-facing view of sales, profit, and customer metrics, 
allowing stakeholders to compare any selected year against the previous year and 
quickly spot over/under-performing categories, products, and customer segments.

## Dashboards
- **Sales Dashboard**: KPI summary (Total Sales, Profit, Quantity) with year-over-year 
  trend lines, subcategory-level sales vs. profit comparison, and weekly sales/profit 
  trend charts highlighting above/below-average periods
- **Customer Dashboard**: Customer distribution, top customers by sales, and 
  sales-per-customer metrics

## Key Features
- **Dynamic Year Selection**: A parameter-driven year filter lets users pick any year; 
  all KPIs and charts recalculate against the prior year automatically (no hardcoded dates)
- **Year-over-Year % Change**: Custom calculated fields compute percentage differences 
  in sales, profit, quantity, and customer count between the selected year and the year before
- **Above/Below Average Highlighting**: `WINDOW_AVG()` based logic flags whether a given 
  period is performing above or below its own average
- **Min/Max Point Highlighting**: `WINDOW_MAX()` / `WINDOW_MIN()` table calculations 
  highlight the best and worst performing points on trend lines
- **LOD Expressions**: `FIXED` level-of-detail calculations used for customer-count 
  aggregations independent of view granularity
- **Ranking**: `INDEX()` based calculations for ordered comparisons (e.g., top customers)
- **Sales per Customer**: Derived metric (Sales ÷ Distinct Customers) for average 
  customer value tracking

## Tools Used
- Tableau (Desktop/Public)
- Data extract (.hyper) with Order Date, Sales, Profit, Quantity, and Customer fields

## Learning Note
This project was built as part of learning Tableau through a guided course, and 
extended with custom calculated fields (year-over-year logic, average-based highlighting, 
and LOD expressions) to deepen understanding of parameters and table calculations.
