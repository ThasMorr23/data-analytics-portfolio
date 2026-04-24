# eBay Seller Insights

## Overview

This project analyzes eBay seller data to uncover insights into sales performance, pricing trends, and buyer behavior. The goal was to transform raw, unstructured export data into a clean, analysis-ready dataset and build an interactive dashboard to support business decision-making.

The project demonstrates an end-to-end data workflow, including data cleaning, transformation, SQL analysis, and data visualization.

## Business Problem

eBay seller data exports are not analysis-ready and often contain:
- inconsistent formatting
- missing values
- mixed data types
- multi-item order structures

This makes it difficult to accurately analyze:
- revenue trends
- pricing strategies
- geographic performance

This project addresses these challenges by building a structured data pipeline and extracting meaningful insights.

## Tools & Technologies

- Python (pandas) – data cleaning and transformation
- PostgreSQL – data storage and querying
- SQL – data analysis
- Tableau – dashboard visualization

## Data Cleaning & Preparation

Key data challenges addressed:

- Removed non-data rows and formatting artifacts from raw CSV exports
- Standardized column naming conventions
- Converted currency fields from text to numeric format
- Parsed and standardized date fields
- Handled missing values using business logic:
  - dropped rows missing critical identifiers
  - filled missing shipping values
- Resolved multi-item orders by distributing shipping costs across items

Result:
A clean, structured dataset ready for SQL analysis and visualization.

## Data Model

Primary dataset: `orders_clean`

Each row represents a single item sold.

Key fields:
- order_number
- sale_date
- buyer_state
- item_title
- sold_for
- shipping_and_handling
- gross_revenue

## Key Analysis

### Revenue Trends
- Identified monthly revenue patterns and sales distribution over time

### Geographic Insights
- Determined top-performing states by revenue and order volume

### Pricing Insights
- Analyzed average sale price and distribution of item values
- Identified high-value items contributing disproportionately to revenue

### Shipping Impact
- Evaluated contribution of shipping charges to total revenue

## Dashboard

The Tableau dashboard provides an interactive view of:

- Total revenue and sales metrics
- Revenue trends over time
- Top buyer locations
- Item-level pricing insights
![Dashboard](tableau/dashboard_screenshot.png)

## Key Insights

- Revenue is concentrated in a small number of higher-priced items
- Certain states consistently generate higher sales volume
- Shipping costs significantly impact total transaction value
- Sales activity shows clustering rather than uniform distribution over time

## Project Structure

- data/ → raw and cleaned datasets
- notebooks/ → exploratory analysis
- scripts/ → data cleaning pipeline
- sql/ → analysis queries
- tableau/ → dashboard assets

## Future Improvements

- Integrate financial data for profit analysis
- Automate data extraction using eBay APIs
- Expand dataset to include longer time periods
- Build predictive models for pricing optimization
