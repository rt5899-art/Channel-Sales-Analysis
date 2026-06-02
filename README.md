## Project Overview
This repository features a comprehensive business intelligence and data analytics solution developed in Power BI. The project focuses on transforming fragmented, raw business data into interactive, executive-level dashboards that deliver actionable insights, track Key Performance Indicators (KPIs), and support strategic data-driven decision-making.

The architecture is built upon a robust relational data model structured with custom data schemas ([Content_Types].xml, DiagramLayout), distinct thematic presentation layers (BaseThemes/CY24SU10.json), and dynamic reporting assets (StaticResources).

## System Requirements
To view, edit, or deploy this project, ensure your environment meets the following specifications:

Operating System: Windows 10 or Windows 11 (64-bit recommended).

Software Application: Power BI Desktop (Latest version preferred for full theme compatibility).

Data Architecture Components:

[Content_Types].xml for package structure validation.

Report/Layout configurations for visual positioning.

CY24SU10.json theme file for layout styling.

## Tools and Technologies Used
Power BI Desktop: The core development environment used for data modeling, analytical engineering, and dashboard creation.

DAX (Data Analysis Expressions): Utilized to build advanced calculations, time-intelligence metrics, and complex business KPIs.

Power Query (M Language): Employed for Extract, Transform, Load (ETL) processes, including data cleaning, schema enforcement, and staging.

JSON Schema: Used to implement a standardized corporate visual design framework via the CY24SU10.json theme file.

Relational Star Schema: Structured to split data efficiently into dedicated dimension and fact tables for optimal query performance.

## Challenges Faced
Complex Model Mapping: Managing relationships between multi-layered datasets while ensuring strict query efficiency within the DiagramLayout boundaries required precise structural mapping.

Enforcing Visual Consistency: Dynamically integrating the JSON theme (CY24SU10.json) across various custom matrices, multi-row cards, and charts required extensive conditional formatting adjustments.

Performance Optimization: Large volumes of transactional data caused initial performance bottlenecks during DAX calculations. Resolving this required moving filtering logic from measures to the underlying data model.

## Data Insights
Seasonal Performance Waves: Deep time-intelligence analysis revealed predictable, repeating sales cycles, highlighting specific periods of high activity that require optimized inventory planning.

Asset Utilization Clusters: Reviewing geographic and resource-based static assets pinpointed significant performance gaps, showing that a small percentage of core resources drive the majority of business value.

Resource Allocation Gaps: Correlating operational costs with performance metrics exposed clear inefficiencies in how budgets are distributed across underperforming business units.

## Recommendations for Improvement
Transition to a DirectQuery Hybrid Architecture: For business units requiring live monitoring, shift large-scale background data to a DirectQuery or incremental refresh model to reduce data import overhead.

Implement Row-Level Security (RLS): Introduce RLS roles within the Power BI data model to ensure secure, customized dashboard views based on user departments or geographical regions.

Adopt Automated Data Governance: Integrate advanced automated validation tracking into the Power Query staging layer to capture and isolate source data anomalies before they impact production reports.
