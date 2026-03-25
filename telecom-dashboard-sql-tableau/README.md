## Live Interactive Dashboard
Explore the full interactive dashboard here:   
[View on Tableau Public](https://public.tableau.com/app/profile/thasanee.morrissey/viz/Churn_Census_Data/ContiguousUnitedStatesStats)

## Telecom Customer Churn Dashboard (SQL + Tableau)
This project analyzes customer churn patterns for a telecommunications company by combining internal customer data with external census income data. The goal was to identify geographic and economic factors that may influence customer churn and support data-driven decision-making.

## Objective
<p>Identify patterns in customer churn across U.S. states </p>
<p>Analyze relationships between income, monthly charges, and customer tenure</p>
<p>Provide insights to support customer retention strategies </p>

## Tools Used
<p>SQL (PostgreSQL)</p>
<p>Tableau (dashboard design)</p>
<p>Data aggregation and transformation</p>

## Data Sources
<p>Customer churn dataset (internal company data) </p>
<p>U.S. census income data (external dataset) </p>

## Key SQL Work
**The analysis involved building multiple tables and aggregations:**
<p>Created structured tables for census income data </p>
<p>Aggregated average income by state </p>
<p>Ranked states by income levels </p>
<p>Joined customer and location data to analyze monthly charges </p>
<p>Calculated average monthly charges by state </p>
<p>Computed churn metrics by state </p>

## Example transformations included:
<p>Aggregating and ranking income data by state </p>
<p>Joining customer and location tables for analysis </p>
<p>Calculating average monthly charges per state </p>

(SQL queries available in the sql/ folder)

## Dashboard Design
**The dashboard included:**
<p>Average income by state (map visualization) </p>
<p>Churn percentage by state </p>
<p>Average monthly charges by state </p>
<p>Lowest tenure states (customer retention risk) </p>

## Interactive features:
<p>State-level filtering </p>
<p>Tooltips with summary metrics </p>
<p>Multi-panel linked visualizations </p>

## Key Insights
<p>States with lower average income showed higher churn rates </p>
<p>Monthly charges and tenure varied significantly across regions </p>
<p>Geographic segmentation can help identify at-risk customer groups </p>

## Business Impact
**This dashboard can help stakeholders:**
<p>Identify high-risk regions for churn </p>
<p>Develop targeted retention strategies </p>
<p>Align pricing and service strategies with regional economics </p>

## Project Files
<p>sql/ → SQL queries used for data transformation </p>
<p>images/ → dashboard visuals (if available) </p>

## What I Would Do Next
<p>Build a predictive churn model </p>
<p>Deploy the dashboard for real-time monitoring </p>
<p>Incorporate additional demographic variables </p>
