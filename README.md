# 🏨 Hotel Revenue & Booking Performance Dashboard

## 📌 Project Overview

This Power BI project provides an interactive analysis of hotel booking performance, revenue generation, occupancy, pricing, customer booking behavior, and realization performance.

The dashboard is designed to help hotel management and business teams monitor key performance indicators (KPIs), compare booking patterns, identify revenue trends, and analyze property-level performance.

## 🎯 Project Objectives

- Monitor overall hotel revenue and booking performance.
- Analyze **Revenue, RevPAR, ADR, Occupancy %, DSRN, and Realisation %**.
- Compare performance across cities, room types, properties, and booking platforms.
- Track weekly trends and identify changes in key performance metrics.
- Compare weekday and weekend performance.
- Analyze booking platforms and their relationship with ADR and realization.
- Evaluate individual hotel/property performance using detailed metrics.
- Provide interactive filtering for easier business analysis.

---

## 📊 Dashboard KPIs

The main dashboard contains the following key metrics:

| KPI | Description |
|---|---|
| **Revenue** | Total revenue generated from hotel bookings |
| **RevPAR** | Revenue per available room |
| **DSRN** | Daily Sellable Room Nights |
| **Occupancy %** | Percentage of available rooms occupied |
| **ADR** | Average Daily Rate |
| **Realisation %** | Percentage of bookings successfully realized |

The displayed dashboard snapshot shows approximately **1.69bn Revenue**, **7,337 RevPAR**, **2,528 DSRN**, **57.79% Occupancy**, **12.70K ADR**, and **70.14% Realisation** for the selected overall context.

---

## 📈 Dashboard Visualizations

### 1. KPI Summary

The KPI section provides a quick overview of the hotel's overall performance using Revenue, RevPAR, DSRN, Occupancy %, ADR, and Realisation %.

A weekday/weekend comparison table is also included to highlight differences in performance between day types.

### 2. Revenue by Category

A donut chart presents the distribution of revenue across hotel categories such as:

- Luxury
- Business

This allows users to understand the contribution of each hotel category to total revenue.

### 3. Trends by Key Matrix

A weekly trend visualization tracks:

- RevPAR
- ADR
- Occupancy %

The week number is used to analyze changes across the reporting period, making it easier to identify weekly performance movements.

### 4. Realisation % and ADR by Booking Platform

A combination chart compares:

- **Realisation %** using columns
- **ADR** using a line

Booking platforms include examples such as:

- LogTrip
- Journey
- Direct Online
- Direct Offline
- Others
- MakeYourTrip
- Tripster

This visual helps compare booking-channel performance with pricing levels.

### 5. Property-Level Performance Matrix

The detailed property table provides granular performance information for individual hotels.

The table includes metrics such as:

- Property ID
- Property Name
- City
- Revenue
- RevPAR
- Occupancy %
- ADR
- DSRN
- DBRN
- DURN
- Cancellation %
- Average Rating
- Realisation %

This enables users to investigate differences between properties and identify areas requiring further analysis.

---

## 🎛️ Interactive Filters

The dashboard provides interactive slicers for:

- **City**
- **Room Type**
- **Week Number**

These filters allow users to dynamically explore the dashboard and analyze specific locations, room categories, or reporting weeks.

---

## 🗂️ Data Model

The Power BI model follows a fact-and-dimension structure.

### Dimension Tables

#### `dim_hotels`

Contains hotel/property master information:

- `property_id`
- `property_name`
- `city`
- `category`

#### `dim_rooms`

Contains room-related information:

- `room_id`
- `room_class`

#### `dim_date`

Provides the date dimension used for time-based analysis:

- `date`
- `Day Type`
- `mmm yy`
- `wn`

The date dimension supports weekly and date-based reporting.

### Fact Tables

#### `fact_bookings`

Contains individual booking-level information:

- `booking_date`
- `booking_id`
- `booking_platform`
- `booking_status`
- `check_in_date`
- `checkout_date`
- `no_guests`
- `property_id`
- `ratings_given`
- `revenue_generated`
- `revenue_realized`
- `room_category`

#### `fact_aggregated_bookings`

Contains aggregated room-booking information:

- `capacity`
- `check_in_date`
- `property_id`
- `room_category`
- `successful_bookings`

---

## 🧮 DAX Measures

The report uses DAX measures to calculate and analyze business KPIs.

Measures visible in the Power BI model include:

- Revenue
- Revenue WoW Change %
- RevPar
- RevPar WoW Change %
- Realisation %
- Realisation WoW Change %
- Total Bookings
- Total Cancelled Bookings
- Total Capacity
- Total Checked Out
- Total No Show Bookings
- Total Successful Bookings

The **WoW (Week-over-Week)** measures enable comparison between the current reporting week and the previous week.

The model also uses a dedicated date dimension with a **week number (`wn`)** field for weekly analysis.

---

## 🔍 Key Analytical Areas

The dashboard supports analysis of several important hospitality business questions:

### Revenue Performance
Understand total revenue generation and compare revenue across properties, cities, categories, and time periods.

### Pricing Performance
Use **ADR** and **RevPAR** to evaluate room pricing and revenue generated relative to available room inventory.

### Occupancy
Analyze how effectively available rooms are being utilized across different properties and periods.

### Booking Channel Performance
Compare realization and ADR across different booking platforms to understand booking-channel behavior.

### Cancellation & No-Show Analysis
Use booking status measures and cancellation percentages to evaluate lost booking opportunities.

### Property Performance
Drill into individual properties to compare revenue, occupancy, ADR, realization, cancellations, ratings, and room-night metrics.

---

## 🛠️ Tools & Technologies

- **Microsoft Power BI**
- **Power Query**
- **DAX**
- Data Modeling
- Interactive Slicers
- KPI Cards
- Donut Charts
- Combination Charts
- Trend Analysis
- Matrix/Table Visualizations

---

## 📁 Suggested Repository Structure

```text
Hotel-Revenue-Booking-Analytics/
│
├── Hotel_Revenue_Booking_Dashboard.pbix
├── README.md
│
└── screenshots/
    └── dashboard.png
```

---

## 💡 Business Value

This dashboard transforms hotel booking and revenue data into an interactive business intelligence solution. It provides management with a consolidated view of financial performance, room utilization, pricing, booking behavior, and property-level results.

By combining KPI monitoring, time-series analysis, booking-platform analysis, and detailed property-level reporting, the report supports faster identification of performance patterns and areas requiring further investigation.

---

## 👨‍💻 Project Skills Demonstrated

This project demonstrates practical experience in:

- Data modeling
- DAX measure development
- Time intelligence
- KPI development
- Power Query data preparation
- Interactive dashboard design
- Hospitality revenue analytics
- Booking and occupancy analysis
- Business performance reporting
- Data visualization
- Exploratory and diagnostic analysis

---

## 📸 Dashboard Preview

Add the exported dashboard screenshot to the repository and reference it below:

```markdown
![Hotel Revenue & Booking Performance Dashboard](screenshots/dashboard.png)
```

---

## 📌 Conclusion

The **Hotel Revenue & Booking Performance Dashboard** provides a centralized analytical view of hotel operations and financial performance. It combines revenue, occupancy, pricing, booking, cancellation, realization, and property-level metrics into an interactive Power BI reporting solution.
