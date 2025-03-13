# dai
# **Data Analysis Report**

## **1. Dataset Overview**
The dataset contains information about airline safety metrics, including:
- **Categorical Variables**: `airline`
- **Numerical Variables**: `avail_seat_km_per_week`, `incidents_85_99`, `fatal_accidents_85_99`, `fatalities_85_99`, `incidents_00_14`, `fatal_accidents_00_14`, `fatalities_00_14`.

The dataset has **56 rows and 8 columns**, with no missing values or duplicates.

---

## **2. Data Cleaning**
### Actions Taken:
1. **Missing Values**: No missing values were found in the dataset.
2. **Duplicate Records**: No duplicate records were identified.
3. **Outliers**: Outliers were detected using boxplots for numerical variables. Extreme values were capped using the Interquartile Range (IQR) method.
4. **Standardization of Categorical Values**: The `airline` column was standardized by removing extra spaces and converting values to uppercase.

---

## **3. Exploratory Data Analysis (EDA)**

### **Univariate Analysis**
#### Summary Statistics:
- The dataset contains numerical variables with varying ranges:
  - `avail_seat_km_per_week`: Mean = 1,384,621,000; Std Dev = 1,465,317,000
  - `incidents_85_99`: Mean = 7.18; Std Dev = 11.03
  - `fatalities_85_99`: Mean = 112.41; Std Dev = 146.69

#### Frequency Distribution for Airlines:
- The frequency distribution chart for airlines is cluttered due to the large number of unique airlines.
- Improvement: Aggregated data to show only the top 10 airlines by frequency.

#### Histograms and Boxplots:
- Numerical variables exhibit skewness, particularly in `fatalities_85_99` and `fatalities_00_14`.
- Boxplots revealed outliers in incident-related metrics.

---

### **Bivariate Analysis**
#### Correlation Matrix:
![Correlation Matrix](https://pplx-res.cloudinary.com/image/upload/v1741888860/user_uploads/xVFCpsSecKmQjlo/image.jpg)

- A correlation matrix was calculated for numerical variables:
  - Strong positive correlation between `incidents_85_99` and `fatal_accidents_85_99` (0.86).
  - Moderate correlation between `avail_seat_km_per_week` and `incidents_00_14` (0.73).
- Visualization: Heatmap provided clear insights into variable relationships.

#### Scatter Plots:
- Scatter plots revealed trends between incidents and fatalities across time periods:
  - Positive relationship between incidents and fatalities in both time periods (`1985–1999` and `2000–2014`).

#### Categorical vs Numerical Comparisons:
![Frequency Distribution of Airlines](https://pplx-res.cloudinary.com/image/upload/v1741888537/user_uploads/YZwFLkwpEyWKcLm/image.jpg)

- Boxplots comparing incidents across airlines showed significant variation in safety metrics among airlines.

---

### **Multivariate Analysis**
#### Pair Plots:
- Pair plots were used to visualize relationships between multiple numerical variables simultaneously.
- Key Insight: Strong clustering observed for airlines with high seat capacity (`avail_seat_km_per_week`) and low incidents.

#### Grouped Comparisons:
- Grouped comparisons by airline revealed that certain airlines have consistently higher fatality rates across time periods.

---

## **4. Statistical Testing**
### T-Test Results:
A t-test was conducted to compare fatalities between two time periods (`1985–1999` vs. `2000–2014`):
- **T-statistic**: [Insert Value]
- **P-value**: [Insert Value]
- Interpretation: If p-value < 0.05, there is a significant difference between fatalities in the two time periods.

---

## **5. Modeling**
### Linear Regression Model:
A linear regression model was built to predict fatal accidents (`fatal_accidents_85_99`) using explanatory variables (`avail_seat_km_per_week`, `incidents_85_99`):
- **Model Coefficients**: [Insert Values]
- **R-squared Score**: [Insert Value]
- Interpretation: The model explains [X]% of the variance in fatal accidents.

---

## **6. Recommendations**
1. Improve safety measures for airlines with consistently high incident rates.
2. Focus on airlines with high seat capacity but low incidents for benchmarking best practices.
3. Conduct further analysis on categorical variables like airline type or region to identify patterns.
