# PhonePe Digital Payments — Data Analysis

## Overview
A Python-based exploratory data analysis of PhonePe digital payments data across Indian states and districts, covering 2018–2021. The goal was to understand transaction trends, regional adoption, device usage patterns, and demographic factors affecting app usage.

## Data
- State-level transaction data (transactions, amount, ATV, registered users, app opens) — quarterly, 2018–2021
- State-level transaction type breakdown (e.g., peer-to-peer payments, recharge & bill payments, merchant payments)
- District-level transaction data
- District demographic data (population, area, density)
- State-level device brand data (registered users by smartphone brand)

## What I Did
- Loaded and cleaned the datasets using Pandas, handling missing values with median imputation
- Grouped and aggregated transaction data by state, year, and quarter to look at growth trends
- Calculated year-over-year growth in transactions per state
- Found the most-used transaction type per state and quarter
- Merged district transaction data with demographic data to calculate users-to-population ratio
- Identified top-performing districts by transaction volume, and lower-adoption districts (filtered to population > 100,000 to keep the comparison meaningful)
- Analyzed which smartphone brand leads registered users in each state
- Checked correlation between population/density and transaction activity using `.corr()`
- Looked at app engagement via app opens, including opens per registered user, to compare active usage across states
- Built visualizations (bar chart, pie chart, line chart, heatmap) using Matplotlib and Seaborn

## Key Findings
- Telangana and Karnataka showed the highest year-over-year transaction growth in the dataset; Lakshadweep showed the most volatile (and often lowest) growth, likely due to its small base
- Xiaomi was the leading device brand by registered users in most states
- Some districts with high population showed comparatively low users-to-population ratios, suggesting room for further adoption
- App engagement (opens per user) varied notably by state, not always tracking directly with raw transaction volume

## Tech Stack
Python, Pandas, NumPy, Matplotlib, Seaborn

## Notes
This was done as a self-guided learning project to practice EDA, data merging, and visualization in Pandas. Some data quality issues (e.g., mismatched year/quarter ranges between datasets) came up during the analysis and were resolved by checking actual data ranges rather than assuming they matched across files.
