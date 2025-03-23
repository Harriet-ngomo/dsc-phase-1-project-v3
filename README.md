# Aviation Safety Analysis

## Project Overview
As our company expands into aviation, this project aims to analyze accident data to identify **low-risk aircraft** for commercial and private use.

## Data Cleaning Process

### 1. Dropped Columns
- **Dropped 'Aircraft.Category'** (More than 50% missing values)

### 2. Handled Missing Values
- **Categorical Columns** (Replaced missing values with `"Unknown"`)  
  - `Broad.phase.of.flight`  
  - `Publication.Date`  
  - `Engine.Type`  
  - `Report.Status`  
  - `Purpose.of.flight`  
  - `Weather.Condition`  
  - `Aircraft.damage`  
  - `Injury.Severity`  

- **Numerical Columns** (Filled missing values with `0`)  
  - `Total.Fatal.Injuries`  
  - `Total.Serious.Injuries`  
  - `Total.Minor.Injuries`  
  - `Total.Uninjured`  

- **Number of Engines** (Filled missing values with **mode** of the column)  

### 3. Dropped Rows with Critical Missing Values
- Removed rows where any of the following were missing:  
  - `Make`  
  - `Model`  
  - `Location`  
  - `Country`  
  - `Event.Date`  


