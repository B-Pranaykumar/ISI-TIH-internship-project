# Data Analysis and Predictive Modeling of House Sales in India

## Project Overview

This project is part of the **IDEAS Summer Internship Program 2026** and focuses on comprehensive data analysis and predictive modeling of house sales data. The primary objective is to understand key factors influencing house prices through exploratory data analysis (EDA) and develop predictive models.

**Created by:** Koulika Paul  
**Designation:** Project Linked Associate Research Engineer in Statistics  
**Organization:** IDEAS - Institute of Data Engineering, Analytics and Science Foundation

**Done by:** Boddula Pranay Kumar

---

## Dataset Description

The dataset contains **14,620 house sale records** with **16 key features** after preprocessing:

### Features
- **Property Characteristics:**
  - Number of bedrooms (range: 1-33)
  - Number of bathrooms (range: 0-8)
  - Living area (370-13,540 sq ft)
  - Lot area (520-1,074,218 sq ft)
  - Number of floors (1-4)
  - Grade of the house (4-13)
  - Area excluding basement (370-9,410 sq ft)
  - Area of basement (0-4,820 sq ft)

- **Location & Amenities:**
  - Waterfront present (binary: yes/no)
  - Number of views (0-4)
  - Number of schools nearby (1-3)
  - Distance from airport (50-80 units)

- **Property Condition:**
  - Condition of the house (1-5 scale)
  - Built year (1900-2015)

- **Target Variable:**
  - **Price** (₹78,000 - ₹7,700,000)

---

## Data Quality

### Summary Statistics
- **Total Records:** 14,620
- **Duplicate Rows:** 0 (clean dataset)
- **Missing Values:** None (complete dataset)
- **Average Price:** ₹538,932
- **Median Price:** ₹450,000
- **Price Range:** ₹78,000 to ₹7,700,000

### Data Integrity
All columns have appropriate data types:
- Integer columns: id, bedrooms, bathrooms, living area, lot area, waterfront, views, condition, grade, basement area, built year, schools, airport distance
- Float columns: number of floors (decimal values represent stories)

---

## Project Analysis Structure

### Question 1: Data Import & Loading
- Import essential libraries (pandas, numpy)
- Load house sales dataset from CSV
- Display first 5 rows for initial data exploration

### Question 2: Data Inspection
- Analyze dataset dimensions: **(14,620 rows × 16 columns)**
- Verify data integrity: **0 duplicate rows**

### Question 3: Data Types & Missing Values
- All 16 columns are properly typed (int64/float64)
- **Zero missing values** across all features
- Complete dataset with no data cleaning required

### Question 4: Data Cleaning
- Remove unnecessary columns: Date, Longitude, Latitude, Postal Code, Renovation Year, living_area_renov, lot_area_renov
- Retain 16 relevant features for analysis
- Focus on core attributes affecting house prices

### Question 5: Descriptive Statistics
- Generate comprehensive statistical summary (count, mean, std, min, 25%, 50%, 75%, max)
- Identify outliers and data distribution patterns
- Key insights:
  - Average bedrooms: 3 (median: 3)
  - Average bathrooms: 2 (median: 2)
  - Average living area: 2,098 sq ft (median: 1,930 sq ft)
  - Built year avg: 1,971 (median: 1,975)

### Question 6: Grouped Analysis by Bedrooms
- Group houses by number of bedrooms
- Calculate average price for each group
- **Price increases with bedroom count:**
  - 1 bedroom: ₹308,964
  - 3 bedrooms: ₹463,278 (average)
  - 5 bedrooms: ₹775,255
  - 8 bedrooms: ₹1,208,455
  - Premium pricing for properties with 7+ bedrooms

---

## Key Findings

### Price Trends
1. **Strong positive correlation with property size** - Larger homes command higher prices
2. **Bedroom count is a major price driver** - Each additional bedroom significantly increases price
3. **Wide price variance** - Suggests other factors (location, condition, age) heavily influence pricing
4. **Built year impact** - Modern homes tend to have varying prices based on condition

### Data Characteristics
- **Well-distributed dataset** with no missing or duplicate values
- **Some outliers present** - Maximum property has 33 bedrooms (likely data anomaly)
- **Consistent property data** - All features properly recorded and validated

---

## Technologies Used

- **Python 3.x**
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computations
- **Google Colab** - Development environment

---

## Project Structure

```
Data-Analysis-and-Predictive-Modeling-of-House-Sales-in-India/
│
├── README.md (this file)
└── 05_Data_analysis_with_house_sales_data_Summer_2026.ipynb
    ├── Q1: Data Import & Loading
    ├── Q2: Data Inspection
    ├── Q3: Data Types & Missing Values
    ├── Q4: Data Cleaning
    ├── Q5: Descriptive Statistics
    └── Q6: Grouped Analysis by Bedrooms
```

---

## How to Use

1. **Access the Notebook:**
   - Open in Google Colab: [Click here to view on Colab](https://colab.research.google.com/github/B-Pranaykumar/ISI-TIH-internship-project/blob/Data-Analysis-and-Predictive-Modeling-of-House-Sales-in-India/05_Data_analysis_with_house_sales_data_Summer_2026.ipynb)

2. **Download the Dataset:**
   - Access the data from: https://drive.google.com/drive/folders/1gieHICVDBbUKMZiSF4YRQMAJic-w50JM?usp=sharing

3. **Run the Analysis:**
   - Execute all cells sequentially
   - Each cell is self-contained and builds upon previous analysis
   - Output will display insights from data exploration

---

## Next Steps for Predictive Modeling

Based on the exploratory analysis, potential next phases include:

1. **Feature Engineering**
   - Create interaction features between bedrooms, bathrooms, and living area
   - Develop age-based features from built year
   - Scale and normalize numerical features

2. **Model Development**
   - Linear Regression for baseline predictions
   - Advanced models: Random Forest, Gradient Boosting
   - Model evaluation using cross-validation and R² score

3. **Additional Analysis**
   - Correlation analysis between features and price
   - Identification of key price drivers
   - Market segmentation by price ranges

---

## Contact & Credits

**Project Mentor:** Koulika Paul  
**Institution:** IDEAS Foundation  
**Program:** Summer Internship 2026

For questions or feedback regarding this analysis, please refer to the project repository on GitHub.

---

## License

This project is part of the IDEAS Foundation Summer Internship Program. All rights reserved.

---

**Last Updated:** June 2026
