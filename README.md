# ⚡ Energy Consumption BI Project

## Overview
This project presents an end-to-end Business Intelligence solution for analyzing electricity consumption patterns in Portugal using Microsoft Fabric and Power BI.

The solution was developed as part of an academic case study based on public data from E-REDES and includes data ingestion, transformation, semantic modeling, DAX measures, and interactive dashboards for time, geography, voltage level, and external factor analysis.

## Project Goals
The main objective of this project was to transform raw energy consumption data into a structured and interactive analytical solution capable of supporting decision-making.

The analysis focuses on:
- consumption trends over time
- seasonal patterns
- geographic distribution by district and municipality
- differences by voltage level
- impact of external factors such as COVID and holiday periods

## Architecture
The project was developed in Microsoft Fabric with the following components:
- Lakehouse for centralized data storage
- Dataflow Gen2 for data ingestion and transformation
- Semantic model built with a star schema approach
- Power BI report for interactive data visualization

## Data Model
The semantic model follows a **Star Schema** design.

### Fact Table
- `Fact Consumption`

### Dimension Tables
- `Dim Date`
- `Dim Geography`

### Additional Analytical Structures
- Time hierarchy: Year → Quarter → Month
- Geography hierarchy: District → Municipality → Parish
- Label tables for COVID and holiday period analysis

## Data Engineering
The data preparation process included:
- data cleaning and standardization
- column renaming and type correction
- handling invalid keys and surrogate code creation
- filtering and selection of relevant analytical fields
- creation of derived flags for COVID and holiday periods

## Key DAX Measures
Some of the main analytical measures implemented in the model include:
- Total Consumption
- Average Consumption
- Maximum Consumption
- Minimum Consumption
- % YoY Consumption
- % YoY Avg Consumption
- % QoQ Avg Consumption
- % MoM Avg Consumption
- Consumption Volatility
- Consumption Amplitude
- Consumption Variation Coefficient

## Dashboards
The report includes several analytical pages:
- Index page with navigation and KPIs
- District Analysis
- Municipality Analysis
- District & Municipality Detail Analysis
- Time Analysis
- Voltage Level Analysis
- External Factor Analysis

## Key Insights
Some of the main findings from the analysis include:
- energy consumption in Portugal shows relatively stable year-over-year variation
- consumption is heavily concentrated in coastal and urban districts such as Lisbon, Porto, Setúbal, and Aveiro
- higher voltage levels account for slightly more total consumption, while low voltage shows stronger seasonal peaks
- holiday months tend to show slightly higher average consumption than non-holiday months
- the COVID period showed a moderate decrease in average consumption

## Repository Structure
```text
energy-consumption-bi-fabric/
│
├── README.md
├── architecture/
├── docs/
├── images/
└── reports/
