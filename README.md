# Aviation Safety Analysis  

## Overview  
As our company expands into aviation, this project analyzes historical accident data to identify **low-risk aircraft** for commercial and private operations. By understanding accident trends and risk factors, we can make data-driven decisions when selecting aircraft for our fleet.  

## Business Problem  
Aircraft accidents pose significant financial and operational risks. The goal of this analysis is to:  
- Identify aircraft models with the lowest accident rates.  
- Analyze key accident causes and patterns.  
- Provide data-driven recommendations for safer aircraft choices.  

## Data  
The dataset consists of aviation accident records, including details such as:  
- **Aircraft Information**: Make, Model, Engine Type, Number of Engines.  
- **Flight & Accident Details**: Event Date, Location, Purpose of Flight, Weather Conditions.  
- **Accident Outcomes**: Injury Severity, Aircraft Damage, Fatalities, Serious Injuries.    

## Methods  

### 1. Data Cleaning  
To ensure data quality, we performed the following preprocessing steps:  

#### Dropped Columns  
- **Removed 'Aircraft.Category'** (More than 50% missing values).  

#### Handled Missing Values  
- **Categorical Columns** (Replaced missing values with `"Unknown"`)  
  - `Broad.phase.of.flight`, `Publication.Date`, `Engine.Type`, `Report.Status`, `Purpose.of.flight`, `Weather.Condition`, `Aircraft.damage`, `Injury.Severity`.  
- **Numerical Columns** (Filled missing values with `0`)  
  - `Total.Fatal.Injuries`, `Total.Serious.Injuries`, `Total.Minor.Injuries`, `Total.Uninjured`.  
- **Number of Engines** (Filled missing values with the **mode** of the column).  

#### Dropped Rows with Critical Missing Values  
- Removed rows where any of the following were missing:  
  - `Make`, `Model`, `Location`, `Country`, `Event.Date`.  

### 2. Exploratory Data Analysis (EDA)  
The Exploratory Data Analysis (EDA) phase involves statistical summaries and visualizations to understand accident trends and aircraft risks.  

#### Dataset Assessment  
- Used `.info()` to check data types and ensure all expected columns are present.  
- Used `.describe()` to generate numerical summaries of key variables.  
- Verified that the dataset has no missing values using `.isna().sum()`.  
- Identified unique values in categorical columns using `.nunique()` and `.value_counts()`.  
- Checked for duplicate records and decided whether to drop or retain them.  

