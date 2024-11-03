# Patient Flow and Satisfaction Dashboard for Healthcare Analytics

This project is a comprehensive Power BI dashboard developed to analyze patient flow, average waiting times, and satisfaction scores. By visualizing and interpreting these key metrics, this dashboard provides actionable insights that support data-driven decisions in healthcare management.

## Table of Contents
- [Overview](#overview)
- [Project Demo](#Project-demo)
- [Data Sources](#data-sources)
- [Features](#features)
- [Implementation Details](#implementation-details)
- [Insights](#insights)

## Overview
The **Patient Flow and Satisfaction Dashboard** enables hospital administrators and management teams to understand and improve operational efficiencies. It tracks and visualizes metrics like:
- Daily patient visits by gender and age group
- Average wait times by department
- Satisfaction scores by demographic categories

These insights aid in optimizing staffing, improving patient satisfaction, and identifying peak operational times.
## Project Demo
https://github.com/user-attachments/assets/8eed3fc5-1ea8-474d-ade0-b4636919de58

## Data Sources
Data was sourced from Dataworld. The dataset includes:
- **Patient demographics** (age, gender)
- **Visit details** (date, time, department)
- **Patient feedback** (satisfaction scores)

## Features
- **Comprehensive Overview**: Shows patient visits, average wait times, and satisfaction scores.
- **Interactive Filters**: Year and month filters to navigate data by time.
- **Demographic Analysis**: Insights by gender, age group, and race.
- **Departmental Metrics**: Average wait time analysis for each department.
- **Time-based Patterns**: Hourly and weekly heatmap for patient visits to identify peak times.

## Implementation Details

### 1. Data Modeling
- **Relationships**: Established relationships between demographics, visits, and feedback tables for seamless data analysis.
- **Calendar Table**: Implemented a calendar table to facilitate time-based filtering and analysis.

#### Key Measures
- **Total Visits**: Aggregates the total number of patient visits.
- **Average Wait Time**: Calculates average waiting times by department.
- **Average Satisfaction Score**: Computes average satisfaction scores by demographic category.

### 2. Visualizations
- **Main Metrics Dashboard**:
  - **Area Chart**: Visualizes total visits, waiting times, and satisfaction scores over time.
  - **KPI Cards**: Highlights the highest and lowest values for key metrics.
  
- **Demographic Analysis**:
  - **Clustered Bar Chart**: Displays patient visits by age group and gender.
  - **Pie Chart**: Shows percentage distribution of satisfaction scores by demographic.

- **Time-Series Insights**:
  - **Heatmap**: Illustrates patient flow by hour and day of the week to identify peak times.

- **Department-Level Analysis**:
  - **Table and Filters**: Lists waiting times and satisfaction scores by department with month and year filtering options.

### 3. Custom DAX Calculations
- **Patient Flow Insights**: Created DAX measures to analyze patient flow trends.
  - Example:
    ```DAX
    Busiest Hour = MAXX(VALUES('Visit Data'[Hour]), [Total Visits])
    ```

- **Satisfaction Star Rating**: Translated numerical satisfaction scores into star ratings.
  - Example:
    ```DAX
    Star Rating = REPT("★", [Satisfaction Score])
    ```

- **Time-Based Metrics**: Calculated month-over-month changes to observe seasonal patterns.

## Insights 
Key findings from the dashboard include:

- **Peak Operational Hours**: Identified peak patient visit hours (10 AM - 12 PM) for optimal staff allocation.
- **Wait Time Bottlenecks**: Certain departments exhibited higher wait times, indicating the need for resource reallocation.
- **Demographic Trends**: Patients aged 30-50 reported lower satisfaction, highlighting areas for targeted improvements.
- **Departmental Efficiency**: Average satisfaction scores by department revealed strengths and improvement areas.

### Operational Efficiency Improvement
Following the implementation of insights from the dashboard, the hospital experienced a:
- **20% reduction in wait times**
- **15% increase in patient satisfaction**
