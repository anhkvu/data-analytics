# Cyclistic Bike Share Trends in NYC (2019-2020)

**[View the Interactive Dashboard on Tableau Public](https://public.tableau.com/profile/your_username/viz/CyclisticBikeShareTrendsinNYC20192020/Story1)**

![Image](https://github.com/user-attachments/assets/fa0a6de9-1231-4d80-8b8b-e1c7fd4a3be4)

***

**Disclaimer**: This work draws extensively on materials from the **Google Business Intelligence Certificate program**. The work presented here reflects my interpretation and approach. The portfolio structure is inspired by my friend **Michael Neang** (github.com/mneang).

***

# 1. Background / Project Overview
Cyclistic’s Customer Growth Team is preparing a business plan for next year. The objective is to understand how customers use Cyclistic bikes, with a priority on identifying demand across station locations. A BI dashboard will summarize trip records, helping the team make informed decisions about where to expand stations and how to optimize operations.

## Key Business Questions Addressed
* How can customer usage insights inform new station growth?
* Which starting and ending station locations are most in demand?
* How do trip patterns vary by time of day, season, and weather?
* Which factors (location, time, season, weather, subscription type) most impact customer demand?
* How does year-over-year trip growth compare across stations?
* Where does congestion occur, and how might new stations alleviate it?

***

# 2. Technology Architecture Overview

## Tools
* **Database & ETL**: Google BigQuery Sandbox for data processing and aggregation
* **Visualization**: Tableau for dashboard creation
* **Data Sources**:
  * Cyclistic trip dataset (rides, timestamps, trip duration)
  * Geographic data (station lat/long + supplemental zip code / neighborhood info)
  * Weather dataset (daily precipitation, temperature, wind speed)
 
## Workflow
1. Data ingestion and validation of station IDs and BikeIDs
2. ETL and SQL development (aggregation by station, time, and weather conditions)
3. Dashboard design and peer review (focus on maps, tables, growth metrics, and seasonal trends)
4. Development and testing, ensuring compliance, accessibility, and performance

***

# 3. Executive Summary

## Problem
Cyclistic leadership needs customer-driven insights to decide where to expand bike-share stations. Without this, new station placement may be based on assumptions instead of usage patterns.

## Key Insights
* High-demand starting and ending stations by geography
* Popular routes based on trip minutes and congestion patterns
* Seasonal and weather-related usage trends (e.g., rain impact)
* Year-over-year growth in trip volume
* Peak usage periods by time of day and season

## Actionable Recommendations
* Prioritize new stations near congested/high-demand locations
* Adjust bike availability for peak seasonal and hourly usage
* Account for weather impact in operational planning
* Use year-over-year trends to project growth and guide investment

***

# 4. Dashboard Requirements 
* **Station Analysis**
  * Table or map visualizing start and end station usage, aggregated by location
  * Measures of congestion and station-level demand
* **Trip Duration & Destination**
  * Visualization ranking end stations by cumulative trip minutes
  * Breakdown by user type (subscriber vs. customer)
* **Seasonal/Time Trends**
  * Peak usage by hour of day, day of week, and season
  * Demand variation relative to weather conditions (rain, temperature, wind)
* **Growth Analysis**
  * Visualization of year-over-year growth in trip counts
  * Display of seasonal peaks and valleys across multiple months

 ***

 # 5. Caveats and Assumptions
* **Geographic detail**: Trip dataset has only lat/long; additional mapping requires supplemental data.
* **Weather precision**: Weather data is daily (not hourly), so precipitation is assumed to affect the full day.
* **Demand constraints**: Station demand may be limited by available bikes (actual unmet demand may not be visible).
* **Compliance**: No personal data (name, email, phone, address) is used; anonymization is required.

***

# 6. Conclusion
The BI tool will provide an executive-ready dashboard summarizing millions of rides into clear, accessible visualizations. It will enable Cyclistic to evaluate demand at current stations, identify temporal and seasonal usage patterns, and track long-term growth trends.
