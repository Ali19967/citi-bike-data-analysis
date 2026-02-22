# 🚲 NY Citi Bike — User Behavior & Rental Pattern Analysis

> A data analysis project exploring how New Yorkers use the Citi Bike rental service — uncovering patterns in user demographics, trip behavior, station popularity, and rental trends to support smarter business decisions.

---

## 📌 Table of Contents

- [Project Overview](#project-overview)
- [Problem Statement](#problem-statement)
- [Objectives](#objectives)
- [Dataset](#dataset)
- [Tools Used](#tools-used)
- [Project Workflow](#project-workflow)
  - [Step 1: Data Cleaning](#step-1-data-cleaning)
  - [Step 2: Exploratory Data Analysis](#step-2-exploratory-data-analysis)
  - [Step 3: Pivot Tables](#step-3-pivot-tables)
  - [Step 4: Data Visualization](#step-4-data-visualization)
  - [Step 5: Storytelling with Data](#step-5-storytelling-with-data)
- [Key Findings](#key-findings)
- [Business Recommendations](#business-recommendations)
- [Limitations](#limitations)
- [What I Learned](#what-i-learned)
- [Future Scope](#future-scope)
- [Project Structure](#project-structure)
- [Connect](#connect)

---

## Project Overview

Citi Bike is the largest bike-share program in the United States, operating across Manhattan, Brooklyn, Queens, the Bronx, and Jersey City with over 20,000 bikes and 1,300+ stations. Users can sign up for an annual subscription or purchase short-term passes via the Citi Bike app.

This project analyzes real Citi Bike trip data to help key stakeholders — across marketing, product, and operations — make informed, data-driven decisions about user targeting, station management, and service improvement.

---

## Problem Statement

Citi Bike collects large volumes of user and trip data through its app. However, raw data alone doesn't tell a story. The goal of this project is to clean, analyze, and visualize that data to answer five core business questions and surface actionable insights for internal teams.

---

## Objectives

The analysis was designed to answer the following questions:

1. What are the most popular pick-up locations across the city for Citi Bike rental?
2. How does average trip duration vary across different age groups?
3. Which age group rents the most bikes?
4. How does bike rental vary across the two user groups (one-time users vs. long-term subscribers) on different days of the week?
5. Does user age impact the average bike trip duration?

---

## Dataset

| Detail | Info |
|---|---|
| **Source** | Citi Bike (NYC) — course-provided dataset |
| **Rows (raw)** | ~20,000+ |
| **Rows (after cleaning)** | ~16,845 |
| **Format** | Excel / Google Sheets (.xlsx) |
| **Key Columns** | Start Station Name, End Station Name, Trip Duration (mins), User Type, Age, Age Group, Bike ID, Weekday |

> ⚠️ Note: This dataset was provided as part of a structured data analysis course. It represents real-world Citi Bike data but has been adapted for educational use.

---

## Tools Used

| Tool | Purpose |
|---|---|
| **Google Sheets / Excel** | Data cleaning, analysis, pivot tables, visualizations |
| **Pivot Tables** | Summarizing and aggregating data across variables |
| **Charts & Graphs** | Bar charts, column charts, scatter plots, stacked area charts |
| **Google Slides** | Final stakeholder presentation |

---

## Project Workflow

### Step 1: Data Cleaning

Raw data is rarely ready for analysis. Before drawing any insights, the dataset went through a thorough cleaning process.

**Issues identified and resolved:**

- **Duplicate records:** Found and removed 3,500+ duplicate rows using the Remove Duplicates function. Empty rows left behind post-removal were also deleted by filtering for blanks.
- **Missing values:** Filtered column F (End Station Name) for blank cells and deleted all rows containing missing data to ensure clean, reliable analysis.
- **Outliers:** After calculating descriptive statistics, unrealistic values were detected — for example, a trip duration of 6,525 minutes (~4.5 days) and an implausibly high user age. These rows were sorted and removed to prevent skewed results.

**Key takeaway:** Data cleaning consumed the most time in this project — a reflection of real-world data analytics where clean data is the foundation of trustworthy insights.

---

### Step 2: Exploratory Data Analysis

With a clean dataset in hand, descriptive statistics were calculated to understand the shape and spread of key variables.

**Statistics calculated for Trip Duration (mins) and User Age:**

| Statistic | Trip Duration (mins) | User Age |
|---|---|---|
| Mean | — | — |
| Median | — | — |
| Minimum | — | — |
| Maximum | — | — |

> 📝 Values intentionally left blank — refer to the dataset file for exact figures.

These calculations helped identify the average Citi Bike user profile and flag any remaining anomalies in the data before moving to pivot analysis.

---

### Step 3: Pivot Tables

Four pivot tables were created to answer the core business questions, each exported into a separate sheet for clarity.

**Pivot Table 1 — Top 20 Pick-Up Locations**
Calculated the frequency count of each start station name to identify the most popular pick-up points across the city.

**Pivot Table 2 — Average Trip Duration by Age Group**
Calculated the mean trip duration in minutes for each age group to understand how long different demographics tend to ride.

**Pivot Table 3 — Bike Rentals by Age Group**
Counted the number of unique bike rentals (by Bike ID) per age group to identify the most active renting demographic.

**Pivot Table 4 — Rentals by User Type and Weekday**
Cross-tabulated bike rentals by day of the week and user type (Subscriber vs. One-Time User) to reveal behavioral differences between the two groups.

---

### Step 4: Data Visualization

Data visualizations were created directly in Google Sheets to transform pivot table outputs into easily digestible charts.

| Visualization | Type | Question Answered |
|---|---|---|
| Top 20 pick-up stations | Bar Chart | Most popular rental locations |
| Average trip duration by age group | Column Chart | How age group affects trip length |
| Bike rentals by age group | Bar Chart | Which age group rents the most |
| Rentals by user type & weekday | Stacked Stepped Area Chart | Subscriber vs. one-time user patterns |
| Age vs. trip duration | Scatter Plot | Correlation between age and trip duration |

Each chart was customized with descriptive titles to make them presentation-ready and accessible to non-technical stakeholders.

---

### Step 5: Storytelling with Data

The final step brought everything together into a structured narrative. Insights were framed around a clear audience (Citi Bike business stakeholders across marketing, product, sales, and leadership) and organized into a Google Slides presentation covering:

- **Scene setting:** The business problem and why the data matters
- **Key findings:** Answers to each of the five original questions
- **Action points:** Specific, practical recommendations for each insight
- **Visualizations:** Charts embedded to support every major point

The goal was not just to present numbers, but to tell a story that stakeholders could act on.

---

## Key Findings

1. **Grove St Path** is the most popular Citi Bike pick-up station by a significant margin, followed by Exchange Place.
2. Users aged **75+** take the longest trips on average, but they are among the least frequent renters.
3. The **35–44 age group** rents the most bikes overall, making them the most active user segment.
4. **Long-term subscribers** dominate weekday usage, while **one-time users** show a notable spike in rentals on weekends.
5. There is **no strong correlation** between user age and trip duration when looking at individual data points — most trips are short regardless of age, with outlier-length trips concentrated in the 30–55 bracket.

---

## Business Recommendations

Based on the analysis, here are suggested action points for key teams at Citi Bike:

- **Station Planning:** Prioritize bike availability and maintenance at high-demand stations like Grove St Path and Exchange Place, particularly during peak hours.
- **Marketing:** Focus acquisition campaigns on the 35–44 demographic who are the most active renters. Consider loyalty or rewards features tailored to this group.
- **Subscriber Growth:** Since one-time users are most active on weekends, targeted weekend promotions or trial offers could be an effective conversion strategy to move them toward annual subscriptions.
- **Product:** The 75+ age group takes longer rides but rents infrequently — exploring accessibility-focused features or senior membership plans could unlock an underserved segment.

---

## Limitations

- The dataset was adapted for educational purposes and may not fully reflect current real-world Citi Bike data.
- Missing and duplicate records were deleted rather than imputed, which may have introduced minor bias.
- The scatter plot analysis was visual and descriptive — no statistical correlation tests (e.g. Pearson coefficient) were applied to confirm or deny the age-duration relationship formally.
- The dataset does not include geographic coordinates, limiting location-based analysis beyond station names.

---

## What I Learned

- The importance of iterative data cleaning — outliers were only discovered after running descriptive statistics, requiring a second round of cleaning.
- How pivot tables can quickly answer complex business questions without writing a single line of code.
- That data visualization is as much about communication as it is about accuracy — choosing the right chart type matters.
- How to translate raw findings into a stakeholder-ready narrative using the data storytelling framework.

---

## Future Scope

If this project were extended, here is what could be added:

- **Python (Pandas):** Re-do the data cleaning and EDA in a Jupyter Notebook for a more reproducible, scalable workflow.
- **Statistical Analysis:** Apply correlation tests to formally validate or reject the age-trip duration hypothesis.
- **Time Series Analysis:** Explore how rental patterns change across months or seasons.
- **Geospatial Visualization:** Map pick-up and drop-off stations using tools like Folium or Tableau to identify geographic demand clusters.
- **Dashboard:** Build an interactive dashboard in Tableau or Power BI for stakeholder self-service exploration.
  
---

*This project was completed as part of a structured data analytics course. All analysis was conducted independently.*
