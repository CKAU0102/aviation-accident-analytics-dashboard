# ✈️ Aviation Accident Analytics Dashboard

 

## Overview

 

This project demonstrates an end-to-end Business Intelligence and Analytics solution built using Power BI, Power Query, DAX and Python.

 

The dataset contains historical aviation accident records collected over multiple decades, including accident details, aircraft information, operator information, geographical locations and free-text accident narratives.

 

The objective of this project was to transform raw and largely unstructured aviation accident data into a structured analytical model that supports executive reporting, geographical analysis, aircraft risk analysis and root-cause investigation.

 

---

 

## Business Questions

 

This dashboard was designed to answer four key questions:

 

- What happened?

- Where did it happen?

- What aircraft were involved?

- Why did it happen?

 

---

 

## Dataset Challenges

 

Several data quality and modelling challenges were identified before dashboard development:

 

### 1. Free-Text Accident Narratives

 

The dataset did not contain a standardized accident-cause field.

 

Example:

 

- Aircraft struck by lightning

- Aircraft impacted a mountain

- Engine caught fire during flight

 

To support root-cause analysis, a rule-based classification framework was created:

 

```text

Summary

↓

Summary_Category

↓

Summary_Main_Cause

```

 

Examples:

 

```text

Weather

CFIT

Mechanical Failure

Collision

Fire / Explosion

```

 

### 2. Highly Granular Aircraft Types

 

The source dataset contained hundreds of aircraft models.

 

Examples:

 

```text

Boeing 747

Douglas DC-3

Antonov AN-24

```

 

To support business-friendly reporting, aircraft were grouped into higher-level categories:

 

```text

Fixed-Wing Aircraft

Military Aircraft

Helicopter

Airship

Flying Boat / Seaplane

```

 

### 3. Inconsistent Location Information

 

Location values contained countries, cities, oceans and descriptive text.

 

Additional attributes were derived:

 

```text

Country

Region

Location_Type

```

 

---

 

## Data Model

 

The solution was designed using a Star Schema.

 

```text

DimDate

|

|

DimLocation ---- FactAircraftAccident ---- DimAircraft

|

|

DimOperator

```

 

### Why Star Schema?

 

- Simpler filtering

- Cleaner DAX calculations

- Better maintainability

- Easier business understanding

- Scalable analytical model

 

---

 

## Dashboard Pages

 

### 1. Executive Overview

 

Provides a high-level summary of:

 

- Total Accidents

- Total Fatalities

- Fatality Rate

- Average Fatalities

- Historical Trends

- Severity Distribution

 

### 2. Geographic Analysis

 

Answers:

 

```text

Where did accidents occur?

```

 

Features:

 

- Global Accident Map

- Top Countries by Accidents

- Top Countries by Fatalities

- Regional Analysis

- Location Type Analysis

 

### 3. Aircraft Analysis

 

Answers:

 

```text

What aircraft were involved?

```

 

Features:

 

- Top Manufacturers by Accidents

- Accidents by Aircraft Category

- Fatalities by Aircraft Category

- Fatality Rate by Aircraft Category

 

### 4. Root Cause Analysis

 

Answers:

 

```text

Why did accidents happen?

```

 

Features:

 

- Accidents by Main Cause

- Fatalities by Main Cause

- Accidents by Summary Category

- Fatality Rate by Main Cause

 

### 5. Advanced Root Cause Analysis

 

Implemented using Power BI Decomposition Tree.

 

Allows interactive drill-down across:

 

```text

Main Cause

↓

Summary Category

↓

Aircraft Category

↓

Region

↓

Severity

```

 

---

 

## Key Insights

 

### Geographic Findings

 

- The Americas represent the largest concentration of accident events.

- Accident frequency and fatality impact are not always aligned across countries.

 

### Aircraft Findings

 

- Fixed-Wing Aircraft account for the majority of accidents and fatalities.

- Accident volume and fatality rate reveal different risk perspectives.

 

### Root Cause Findings

 

- Environment / Terrain and Technical / Mechanical factors are major accident drivers.

- Categories with the highest accident counts are not always the categories with the highest fatality rates.

 

### Overall Insight

 

Accident frequency and accident severity are not necessarily the same thing. Therefore, accident counts, fatalities and fatality rates should be analyzed together to provide a balanced view of aviation risk.

 

---

 

## Technology Stack

 

- Power BI

- Power Query (M)

- DAX

- Python

- Dimensional Modelling

- Star Schema Design

 

---

 

## Skills Demonstrated

 

### Analytics Engineering

 

- Data Profiling

- Data Cleansing

- Data Standardization

- Business Rule Design

 

### Data Modelling

 

- Star Schema

- Fact & Dimension Modelling

- Semantic Layer Design

 

### Business Intelligence

 

- KPI Design

- Dashboard Development

- Data Visualization

- Analytical Storytelling

 

### Advanced Analytics

 

- Root Cause Analysis

- Classification Framework

- Decomposition Tree Analysis

 

---

 

## Future Improvements

 

If additional time and data were available:

 

- Integrate flight volume and passenger traffic data

- Calculate exposure-based safety metrics

- Apply NLP techniques for automated accident cause classification

- Deploy through Power BI Service with scheduled refresh and Row-Level Security (RLS)

 

---

 

## Screenshots

 

Dashboard screenshots are available in the `screenshots` folder.

 
