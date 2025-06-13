# 🏔️ Global Ski Resort Insights Dashboard

An interactive Power BI dashboard analyzing 102K+ ski resorts across 6 continents, providing insights into elevation levels, beginner and difficult slopes, child-friendly options, night and summer skiing availability, and more.

## 📊 Overview

This project visualizes and analyzes ski resort data to identify global trends using Power BI. The dashboard helps users explore resorts by country and continent with rich visualizations and interactivity.

## 📌 Business Problem

Ski tourism companies, adventure travelers, and tourism analysts often lack a centralized, visual platform to compare resorts globally. This dashboard solves that by delivering powerful insights on slope profiles, seasonal facilities, and terrain elevations across continents.

## 🚀 Key Features

- Analysis of **102K+ ski resorts** across 6 continents
- **10+ custom DAX measures** for KPI calculation
- **12+ interactive visuals**: bar, pie, line, and map charts
- Continent-level slicers, drill-through filters for deeper exploration
- Advanced UX: KPI cards, tooltips, conditional formatting

## ⚙️ Tech Stack

- **Power BI** (DAX, Power Query)
- **Excel** (for preprocessing)
- **Python (optional)** – for data cleanup (if used)
- **Data Source**: CSV/XLSX format (imported into Power BI)

## 🖼️ Screenshots

> _(Include dashboard image here)_  
> ![Dashboard Screenshot](https://github.com/sakibsadri/Global-Ski-Resort-Insights-Dashboard-/blob/main/Global-Ski-Resort-Insights-Dashboard.jpg)

## 📈 Sample DAX Measures Used

```DAX
Average Beginner Slopes = AVERAGE(SkiResortsData[BeginnerSlopes])
Child Friendly Resorts = CALCULATE(COUNTROWS(SkiResortsData), SkiResortsData[IsChildFriendly] = TRUE)
Avg Elevation Gain = AVERAGE(SkiResortsData[HighestPoint] - SkiResortsData[LowestPoint])
Average Beginner Slopes = AVERAGE(SkiResortsData[BeginnerSlopes])
Avg Elevation Gain = AVERAGE(SkiResortsData[HighestPoint] - SkiResortsData[LowestPoint])
Resorts with All Features =
CALCULATE(
  COUNTROWS(SkiResortsData),
  SkiResortsData[IsChildFriendly] = TRUE,
  SkiResortsData[HasNightSkiing] = TRUE,
  SkiResortsData[HasSummerSkiing] = TRUE
)
