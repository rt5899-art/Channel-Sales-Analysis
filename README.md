# Channel Sales Analysis 


## Project Overview

This repository hosts a multi-channel supply chain and sales performance analysis project built in Microsoft Power BI. The main purpose of this project is to aggregate complex distribution logistics, operational margins, and warehouse transaction metrics into a unified business intelligence interface. By evaluating performance indicators across fulfillment hubs and diverse transaction routes, this project addresses the problem of fragmented B2B and B2C operational data, enabling supply chain managers to optimize discount applications, track seasonal ordering patterns, and eliminate warehouse distribution imbalances.

### Requirements

Microsoft Power BI Desktop (Version 2.126 or higher recommended)

System memory: Minimum 8 GB RAM (16 GB recommended for seamless tabular data calculations)

Operating System: Microsoft Windows 10 or Windows 11

Data Source File: Cleaned supply chain ledger records and distribution matrix files (CSV or Excel format)

### Tools and Technologies

Business Intelligence Platform: Microsoft Power BI

ETL Transformation Engine: Power Query

Analytical Expression Language: DAX (Data Analysis Expressions)

Data Architecture: Local Star Schema Relational Model

### Challenges Faced

Overlapping Text in Saturated Matrices: Displaying multi-digit alphanumeric warehouse tracking numbers (e.g., WARE-NMK1003, WARE-PUJ1005) next to massive raw revenue fields led to matrix truncation. This was fixed by setting auto-fit column constraints, adjusting header alignment padding, and reducing text formatting to appropriate decimal limits.

Complex Multi-Channel Donut Mapping: Segmenting independent order volumes simultaneously by physical warehouse locations and variable sales channels caused rendering lag during cross-filtering. This was resolved by optimizing relationships between fact and dimension tables and disabling bi-directional cross-filtering where unnecessary.

Syncing Dual-Axis Discrepancies: Overlaying continuous trend charts with dynamic numeric callouts across a 12-month calendar created formatting conflicts. This was solved by designing custom tooltips to isolate granular value changes smoothly across months.

### Key Insights

Dashboard

![image alt](https://github.com/rt5899-art/Channel-Sales-Analysis/blob/main/ss-%20Channelsales%20dash_bi.png?raw=true)

Based on the aggregated data compiled in the data model interface, the following insights regarding distribution networks and revenue performance were identified:

High-Level Distribution Key Performance Indicators: The platform monitors an overall Total Sales volume of 82.69M, generating a Total Profit of 30.87M. This output is generated across a Total Unit Sold volume of 36K, bringing in an Average Profit of 3.86K per transaction with an Avg Delivery Days rate of 15.17 days.

Temporal Revenue Velocity: Continuous revenue flow analysis shows clear seasonal variations. The fiscal calendar opens with a multi-month decline, falling from 6.2M in February down to a cycle low of 4.5M in April. Immediately following this valley, revenue experiences continuous upward growth, peaking at 8.1M in July and maintaining an elevated baseline through the remainder of the year before closing at 8.4M in December.

Order Footprint by Warehouse Hub: Orders are distributed across six main warehouse hubs. WARE-NMK1003 captures the largest individual share of fulfillment tracking, logging 2,505 Total Orders, 11,351 in Total Quantity, 2,61,07,132.90 in Revenue, and 97,52,837.39 in Total Profit. WARE-PUJ1005 follows with 1,451 Total Orders and 56,06,478.12 in Total Profit. The remaining facilities scale down gradually, with WARE-NBV1002 representing the smallest distribution footprint at 691 Total Orders and 26,03,580.10 in Total Profit.

Sales Channel Volume and Profit Performance: Market distribution paths display distinct volume dynamics:

Distributor channels command the largest operational volume share, capturing 41.14% of orders (reflecting 6,287 Total Orders, a 55,28,657.54 Total Profit, and an Average of Discount Applied of 0.11).

Online channels capture a 30.13% order share (reflecting 2,425 Total Orders, 90,98,012.94 in Total Profit, and a 0.12 discount profile).

In-Store physical retail channels capture a 17.39% order share but generate the highest overall financial yield, securing 1,27,35,062.34 in Total Profit from 3,298 orders.

Wholesale operations represent the smallest share at 11.34% of orders, bringing in 35,12,924.90 in Total Profit.

Monthly Order Pacing: Order quantity counts track distinct cyclical movements throughout the year. Volume hits its lowest point in March at 449 orders before staging a continuous monthly expansion through summer, peaking at 795 orders in July, and stabilizing at 791 orders in December.

### Recommendations for Improvements

Replicate In-Store Margin Efficiencies Across Digital Channels: In-Store retail channels represent an incredibly profitable sector, securing a peak Total Profit of 1,27,35,062.34 from 3,298 orders. Management should conduct a complete pricing structure audit to see if this margin efficiency can be applied to Distributor channels (which handle 6,287 orders but bring in less than half the profit at 55,28,657.54).

Audit Warehouse Logistics at WARE-NMK1003: Since WARE-NMK1003 is the primary logistics hub for the network—handling 2,505 orders and generating a dominant 97,52,837.39 in profit—operations should review this facility's storage and distribution processes. Creating a playbook based on these findings will help optimize lower-performing sites like WARE-NBV1002 (26,03,580.10 profit).

Optimize Discount Allocations to Capitalize on Peak Ordering Windows: The system records a long, steady increase in order volume starting from the March valley (449 orders) through the July peak (795 orders). Tightening the Average of Discount Applied from the current 0.12 baseline down to 0.09 during high-demand months would directly increase net margins when demand is already high.

Address the Q1 Revenue Valley: The dashboard highlights a sharp revenue drop between February (6.2M) and April (4.5M). Cross-referencing this drop with seasonal marketing data and inventory logs will help identify if the decline is a standard seasonal trend or if it points to inventory stockouts that need to be resolved.
