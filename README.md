# National Accounts Statistics of India Using Python

## 1. Project Overview

The project focuses on cleaning, analysing, and visualizing India's National Accounts Statistics using Python. The main objective is to understand GDP trends at Current Prices and Constant Prices through data preprocessing, Exploratory Data Analysis (EDA), feature engineering, descriptive statistical analysis, and data visualization.

## 2. Objectives

- Understand the structure of the National Accounts Statistics dataset.
- Identify and handle missing values.
- Detect and remove duplicate records.
- Check and correct data types where required.
- Standardize column names and data formats.
- Perform Initial EDA and Final EDA.
- Create new features using feature engineering.
- Calculate descriptive statistical measures.
- Analyse GDP trends at Current Prices and Constant Prices.
- Perform correlation analysis.
- Create meaningful visualizations.
- Identify important patterns and insights from the dataset.

## 3. Tools and Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn

## 4. Dataset Description

The project uses the National Accounts Statistics of India dataset.

**Original Dataset:**
- Rows: 7,836
- Columns: 13

The dataset contains information related to financial years, GDP indicators, industries, institutional sectors, and price measures.

### Dataset Columns

1. Base_Year
2. Series
3. Year
4. Indicator
5. Frequency
6. Revision
7. Industry
8. SubIndustry
9. Institutional_Sector
10. Quarter
11. Current_Price
12. Constant_Price
13. Unit

## 5. Data Preprocessing

Data preprocessing was performed to improve the quality and consistency of the dataset.

The following operations were carried out:

- Inspected the dataset structure.
- Checked missing values.
- Identified duplicate records.
- Removed 15 duplicate records.
- Examined data types.
- Checked data consistency.
- Standardized column names and formats where required.
- Handled missing values.

### Dataset After Data Cleaning

- Original Rows: 7,836
- Duplicate Records Removed: 15
- Final Rows: 7,821
- Original Columns: 13

## 6. Exploratory Data Analysis (EDA)

Initial EDA was performed to understand the original dataset, its structure, numerical columns, missing values, and duplicate records.

Final EDA was performed after data cleaning and feature engineering to examine the quality and characteristics of the processed dataset.

The analysis included:
- Dataset information and structure.
- Numerical summaries.
- Missing value inspection.
- Duplicate record inspection.
- Distribution of numerical variables.
- Analysis of GDP at Current Prices and Constant Prices.

## 7. Feature Engineering

Feature engineering was performed to create additional columns from the existing financial-year information.

Three new columns were created:

| New Column | Purpose |
|---|---|
| Year_start | Extracts the starting year from the financial year. |
| Year_end | Extracts the ending year from the financial year. |
| Period_type | Identifies the type of period represented in the year field. |

### Dataset After Feature Engineering

- Total Rows: 7,821
- Original Columns: 13
- New Columns: 3
- Final Columns: 16

These additional columns help organize financial-year information and support year-wise analysis.

## 8. Data Validation

Data validation was performed to check the quality and consistency of the cleaned dataset before proceeding with statistical analysis.

The following checks were considered:

- Missing Value Check: Checked whether missing values remained after data cleaning.
- Duplicate Check: Verified duplicate records after removing 15 duplicate entries.
- Data Type Check: Examined column data types to ensure they were suitable for analysis.
- Data Consistency Check: Checked the consistency of values and formats in the dataset.

The final cleaned dataset was used for further statistical analysis and visualization.

## 9. Statistical Analysis

Descriptive statistical analysis was performed to understand the numerical characteristics of GDP at Current Prices and Constant Prices using 7,821 observations.

### Descriptive Statistics

The following measures were calculated using the describe() function.

| Measure | Current Price | Constant Price |
|---|---:|---:|
| Count | 7,821 | 7,821 |
| Mean | 2,197,954.19 | 1,281,543.94 |
| Standard Deviation | 4,584,007.05 | 2,908,893.67 |
| Minimum | -1,345,477.98 | -419,196.77 |
| 25% (Q1) | 67,624.55 | 13.34 |
| Median (Q2) | 609,067.50 | 323,158.57 |
| 75% (Q3) | 2,197,954.19 | 1,279,090.76 |
| Maximum | 36,204,793.61 | 32,312,034.24 |

### Measures of Central Tendency

Mean and Median were calculated to understand the central values of GDP.

**Interpretation:**

- Current-price GDP has a higher mean and median than constant-price GDP.
- For both variables, the mean is higher than the median.
- This indicates that high-value observations influence the average values.

### Measures of Dispersion

Standard deviation was calculated to understand the variation in GDP values.

- Current Price Standard Deviation: 4,584,007.05
- Constant Price Standard Deviation: 2,908,893.67

**Interpretation:**

Current-price GDP has a higher standard deviation than constant-price GDP, indicating greater absolute variation in its observed values.

## 10. Data Visualization and Interpretations

Different visualizations were created using Matplotlib and Seaborn to understand GDP patterns, distributions, comparisons, and relationships between Current Prices and Constant Prices.

## Line Chart – Year-wise GDP at Current and Constant Prices

A line chart was created to compare GDP at current prices and constant prices across 15 financial years, from 2011–12 to 2025–26. Different lines were used to represent the two GDP measures.

**Interpretation:**

- GDP at current prices remained higher than GDP at constant prices throughout the observed period.
- Both measures show an overall increasing trend.
- In 2020–21, both GDP measures declined compared with 2019–20.
- A slight decline was also observed in 2023–24.
- Both measures reached their highest displayed values in 2025–26.
- Current-price GDP increased from 1,108,641.10 in 2011–12 to 3,818,356.32 in 2025–26.
- Constant-price GDP increased from 954,304.49 in 2011–12 to 2,756,158.21 in 2025–26.

##  Grouped Bar Chart – Year-wise Comparison of GDP

A grouped bar chart was created to compare GDP at current prices and constant prices side by side for each financial year.

**Interpretation:**

- Current-price GDP is higher than constant-price GDP in all 15 financial years.
- In 2011–12, current-price GDP was 1,108,641.10 and constant-price GDP was 954,304.49.
- In 2015–16, the values increased to 1,659,528.23 and 985,170.21, respectively.
- In 2020–21, both measures showed a decline compared with the previous year.
- In 2022–23, current-price GDP reached 2,933,583.21 and constant-price GDP reached 1,672,463.52.
- The highest displayed values occurred in 2025–26.

## Box Plot – Distribution of GDP at Current and Constant Prices

A box plot was created to compare the distribution, median, spread and potential outliers of GDP at current prices and constant prices.

**Interpretation:**

- The median current-price GDP is approximately 2,286,646.99.
- The median constant-price GDP is approximately 1,222,825.49.
- Current-price GDP has a wider spread of values than constant-price GDP.
- The current-price values range from 1,108,641.10 to 3,818,356.32.
- The constant-price values range from 733,691.06 to 2,756,158.21.
- The box plot displays the highest constant-price observation as a potential outlier.

## Histogram – Distribution of GDP at Current Prices

A histogram was created using GDP values at current prices to understand their frequency distribution across different value intervals.

**Interpretation:**

- The histogram represents 15 financial-year observations.
- The minimum current-price GDP value is 1,108,641.10.
- The maximum current-price GDP value is 3,818,356.32.
- The bars show how frequently GDP values occur within different intervals.
- The observations are spread across several value intervals.
- A high value is observed near 3.82 million.

## Scatter Plot – Relationship Between GDP at Current and Constant Prices

A scatter plot was created using GDP at current prices on the X-axis and GDP at constant prices on the Y-axis to examine the relationship between the two variables.

**Interpretation:**

- The scatter plot represents 15 financial-year observations.
- The points generally follow an upward pattern.
- Current-price GDP ranges from 1,108,641.10 to 3,818,356.32.
- Constant-price GDP ranges from 733,691.06 to 2,756,158.21.
- The Pearson correlation coefficient is 0.9379.
- This indicates a strong positive linear relationship between the two GDP measures.

## Bubble Chart – GDP at Current and Constant Prices

A bubble-style scatter chart was created using current-price GDP on the X-axis and constant-price GDP on the Y-axis. Different colours were used to represent the order of the financial years.

**Interpretation:**

- The chart represents 15 financial-year observations from 2011–12 to 2025–26.
- The colour gradient represents the sequence of financial years.
- Both GDP measures generally increase together.
- The points show an upward pattern.
- Declines can be observed around 2020–21 and 2023–24.
- The correlation coefficient of 0.9379 supports the strong positive relationship between the two measures.

## Multivariate Scatter Plot – GDP Values by Financial Year

A multivariate scatter plot was created using current-price GDP and constant-price GDP. Financial year was included as an additional variable and represented through different colours.

**Interpretation:**

- The chart compares both GDP measures across 15 financial years.
- Different colours help identify the financial-year observations.
- The points show a strong positive upward pattern.
- The highest current-price GDP value is 3,818,356.32 in 2025–26.
- The highest constant-price GDP value is 2,756,158.21 in 2025–26.
- The lowest current-price GDP value is 1,108,641.10 in 2011–12.
- The lowest constant-price GDP value is 733,691.06 in 2013–14.

##  Pair Plot – GDP at Current and Constant Prices

A pair plot was created using the two numerical variables, Current_Price and Constant_Price. Histograms were displayed along the diagonal, while scatter plots were displayed outside the diagonal.

**Interpretation:**

- The diagonal histograms show the individual distributions of the two GDP variables.
- The scatter plots show the relationship between current-price and constant-price GDP.
- The scatter plots display a positive relationship between the two variables.
- Current-price GDP ranges from 1,108,641.10 to 3,818,356.32.
- Constant-price GDP ranges from 733,691.06 to 2,756,158.21.
- The pair plot provides a combined view of distribution and relationship.

## Stacked Bar Chart – GDP at Current and Constant Prices

A stacked bar chart was created to display current-price GDP and constant-price GDP together for each financial year using different colours.

**Interpretation:**

- The chart displays both GDP measures across 15 financial years, from 2011–12 to 2025–26.
- Both measures generally increased over the observed period.
- A decline is visible in 2020–21, followed by an increase in subsequent years.
- In 2025–26, current-price GDP reached 3,818,356.32 and constant-price GDP reached 2,756,158.21.
- In 2011–12, current-price GDP was 1,108,641.10 and constant-price GDP was 954,304.49.
- The stacked bars show the two values together for each year.

## 11. Key Insights and Findings

- The original dataset contained 7,836 records and 13 columns.
- A total of 15 duplicate records were removed.
- The final cleaned dataset contains 7,821 records.
- Feature engineering added three new columns, resulting in 16 columns.
- The mean GDP at Current Prices is 2,197,954.19.
- The mean GDP at Constant Prices is 1,281,543.94.
- Current-price GDP has a higher standard deviation of 4,584,007.05.
- Constant-price GDP has a standard deviation of 2,908,893.67.
- The median GDP at Current Prices is 609,067.50.
- The median GDP at Constant Prices is 323,158.57.
- GDP values generally increased across the 15 financial years from 2011–12 to 2025–26, although some declines occurred.
- The highest annual values in the visualization dataset occurred in 2025–26.
- Pearson correlation analysis showed a strong positive relationship between Current Price and Constant Price GDP, with a correlation coefficient of 0.9379.

## 12. Conclusion

This project provided practical experience in data cleaning, preprocessing, feature engineering, Exploratory Data Analysis, descriptive statistical analysis, correlation analysis, and data visualization using Python.

The analysis helped identify important patterns and relationships between GDP at Current Prices and Constant Prices in India's National Accounts Statistics.

The project also demonstrated how Python libraries such as Pandas, NumPy, Matplotlib, and Seaborn can be used to transform raw data into meaningful statistical insights and visual representations.

## 13. Future Scope

- Perform more detailed time-series analysis.
- Explore GDP trends across different industries.
- Compare GDP across institutional sectors.
- Apply additional statistical techniques.
- Develop predictive models for future GDP trends.
- Create interactive dashboards for better data presentation.


