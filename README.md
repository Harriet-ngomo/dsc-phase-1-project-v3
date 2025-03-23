# Aviation Safety Analysis

## Project Overview
As our company expands into aviation, this project aims to analyze accident data to identify **low-risk aircraft** for commercial and private use.

## Data Cleaning Process
- **Dropped 'Aircraft.Category'** (Too many missing values)
- **Handled Missing Values**:
  - Imputed categorical data with `"Unknown"`
  - Filled missing numerical injury counts with `0`
  - Dropped rows with missing **Event.Date**, **Make**, **Model**

