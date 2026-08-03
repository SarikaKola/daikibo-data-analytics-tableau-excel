# daikibo-data-analytics-tableau-excel

## Overview

This repository contains my completed solutions for the **Deloitte Data Analytics Virtual Job Simulation** on Forage.

The simulation focused on analyzing manufacturing telemetry data using **Tableau** and investigating **gender pay equality** using **Microsoft Excel**.

---

## Tools Used

- Tableau
- Microsoft Excel
- Data Visualization
- Data Cleaning
- Dashboard Design
- Calculated Fields
- Conditional Logic

---

# Task 1 – Manufacturing Telemetry Analysis (Tableau)

## Objective

Analyze telemetry data collected from Daikibo factories to identify machinery downtime and create an interactive dashboard.

### Dataset

- `daikibo-telemetry-data.json`

### Steps Completed

- Imported JSON telemetry dataset into Tableau.
- Enabled all schema levels during import.
- Created a calculated field:

```text
IF [Status] = "unhealthy" THEN 10 ELSE 0 END
```

named:

```
Unhealthy
```

representing **10 minutes of downtime** for every unhealthy telemetry event.

- Created a bar chart showing:

> Down Time per Factory

- Created another bar chart showing:

> Down Time per Device Type

- Built an interactive dashboard linking both visualizations.
- Configured the **Factory chart as a filter**, allowing users to analyze downtime by device type within a selected factory.
- Identified the factory with the highest downtime and captured the dashboard screenshot.

---

## Dashboard

### Features

- Total downtime by factory
- Downtime by machine/device type
- Interactive filtering
- Easy comparison between factories

### Result

- `Dashboard.png`

---

# Task 2 – Gender Pay Equality Analysis (Excel)

## Objective

Classify equality scores for different job roles across Daikibo factories.

### Dataset

- `Data - Equality Table.xlsx`

The dataset contained:

- Factory
- Job Role
- Equality Score

---

## Solution

Added a new column:

```
Equality Class
```

using conditional logic.

### Classification Rules

| Equality Score | Classification |
|---------------|----------------|
| -10 to +10 | Fair |
| -20 to -11 or +11 to +20 | Unfair |
| Less than -20 or Greater than +20 | Highly Discriminative |

### Example Excel Formula

```excel
=IF(ABS(C2)<=10,"Fair",
IF(ABS(C2)<=20,"Unfair",
"Highly Discriminative"))
```

---

### Result
- `Completed Equality Table.xlsx`


## Skills Demonstrated

### Tableau

- JSON Data Import
- Calculated Fields
- Dashboard Design
- Interactive Filters
- Data Visualization
- KPI Analysis

### Excel

- IF Functions
- Logical Operators
- Data Classification
- Conditional Analysis

---

## Project Outcomes

- Identified downtime trends across multiple factories.
- Built an interactive Tableau dashboard for operational monitoring.
- Classified gender equality scores using Excel formulas.
- Applied data analytics techniques to solve real-world business problems.

---


## Author

**Sarika**
