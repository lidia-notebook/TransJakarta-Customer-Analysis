# TransJakarta Data Analysis

##  Project Overview
This project focuses on analyzing **TransJakarta passenger data** to understand travel behavior, demographics, and corridor performance.  
Using **Python** for data wrangling and **visualization**, the goal is to uncover insights that can help improve public transport planning and passenger experience through data-driven decisions.

---

## Objectives
- Analyze ridership trends across time and corridors.  
- Identify **peak travel hours** and **busiest routes**.  
- Understand **passenger demographics** (gender & age).  
- Compute **average trip duration** and **revenue per trip**.  
- Visualize the data through clear, interactive dashboards.

---

##  Dataset Description
- **Source:** TransJakarta public dataset (cleaned & processed locally)  
- **Files Used:**  
  - `tap_in_out.csv` – trip transaction data  
  - `rider_info.csv` – passenger demographics  
  - `corridor_info.csv` – route details  

| Column Name | Description |
|--------------|-------------|
| `tapInTime` | Time passenger tapped in |
| `tapOutTime` | Time passenger tapped out |
| `corridorID` | Corridor (bus route) identifier |
| `corridorName` | Corridor name |
| `payCardSex` | Passenger gender |
| `birthDate` | Passenger birth date ||
 
🗓️ **Date Range:** April 2023 

---

## Data Cleaning & Preparation
Key preprocessing steps performed in Python:

1. **Handle missing values** for time, gender, and age columns.  
2. **Convert data types** (e.g., `tapInTime` and `tapOutTime` → `datetime`).  
3. **Derived new columns:**
   - `hour_bin`: time of day (Early, Morning, Noon, Evening, Night)
   - `age_bin`: age categories (<18, 18–30, 31–45, 46–60, >60)
   - `trip_duration_min`: duration in minutes
4. **Remove invalid trips** (e.g., negative durations, duplicates).  
5. **Rename columns** consistently (e.g., `tapOutTime_Filled`, `corridorID_Filled`).


