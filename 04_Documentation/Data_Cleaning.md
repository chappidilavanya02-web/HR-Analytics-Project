# Data Cleaning and Preparation

## 1. Overview

After completing the initial data quality assessment, statistical outlier investigation and business rule validation, the IBM HR Employee Attrition dataset was prepared for analysis.

The objective was to create a reliable analytical dataset while preserving the original source data.

**Tools Used:**
- Python
- Pandas
- Jupyter Notebook

## 2. Preserve the Original Dataset

The original dataset was loaded into a Pandas DataFrame named `df`.

A separate copy was created for cleaning:

```python
df_clean = df.copy()
```

This ensured that cleaning operations were performed on a separate DataFrame without modifying the original raw dataset.

## 3. Removal of Constant Columns

Three columns were identified as having only one unique value:

| Column | Constant Value | Decision |
|---|---|---|
| EmployeeCount | 1 | Removed |
| Over18 | Y | Removed |
| StandardHours | 80 | Removed |

**Reason for removal:**

These columns contained no variation across employee records and did not provide useful information for the intended analysis.

The columns were removed from `df_clean`. The original dataset remained unchanged.

## 4. Missing Values and Duplicate Records

The original dataset contained:

- Missing values: 0
- Duplicate rows: 0
- Duplicate EmployeeNumber values: 0

Since no missing values or duplicate records were identified, no imputation or duplicate-removal operations were required.

## 5. Outlier Treatment

The Interquartile Range (IQR) method was used to identify potential outliers in selected numerical columns.

The flagged values were investigated using relevant employee attributes and business context.

| Column | Potential Outliers | Cleaning Decision |
|---|---:|---|
| Age | 0 | No outlier treatment required |
| TotalWorkingYears | 63 | Retained after investigation |
| YearsAtCompany | 104 | Retained |
| DistanceFromHome | 0 | No outlier treatment required |
| MonthlyIncome | 114 | Retained after investigation |

**Decision:**

No employee records were removed solely because they were identified as statistical outliers.

High experience, company tenure and income values can represent legitimate employee characteristics.

## 6. Business Rule Validation

Business rule checks were performed to identify potential inconsistencies.

The checks included:

- Age range validation using an assumed general range of 18–65.
- Monthly income greater than zero.
- TotalWorkingYears greater than or equal to YearsAtCompany.
- YearsInCurrentRole not exceeding YearsAtCompany.
- YearsWithCurrManager not exceeding YearsAtCompany.
- EmployeeNumber uniqueness.

The age range was used as a general validation assumption and was not treated as a confirmed company policy.

No records were modified or removed without a documented reason.

## 7. Categorical Data Validation

Text-based categorical columns were checked for:

- Leading and trailing spaces.
- Inconsistent capitalization.
- Unexpected category values.

The checks covered Attrition, BusinessTravel, Department, EducationField, Gender, JobRole, MaritalStatus and OverTime.

No unexpected category values or text inconsistencies were identified.

## 8. Ordinal Variable Validation

The following ordinal-coded columns were checked against their expected value ranges:

- Education
- EnvironmentSatisfaction
- JobInvolvement
- JobLevel
- JobSatisfaction
- PerformanceRating
- RelationshipSatisfaction
- StockOptionLevel
- WorkLifeBalance

The original numerical codes were retained.

These fields represent ordered categories rather than ordinary continuous numerical measurements. Their labels can be used in reporting and visualisation where appropriate.

## 9. Final Dataset Verification

After the cleaning and validation process, the cleaned dataset was checked again.

| Validation | Final Result |
|---|---:|
| Total Records | 1,470 |
| Total Columns | 32 |
| Missing Values | 0 |
| Duplicate Rows | 0 |
| Duplicate EmployeeNumber Values | 0 |
| Remaining Constant Columns | 0 |

No employee records were removed during the cleaning process.

## 10. Export of Cleaned Dataset

The final prepared dataset was exported as a CSV file.

**File name:**

`Cleaned.csv`

**Output folder:**

`02_Cleaned_Data`

This cleaned dataset was subsequently imported into Power BI for data modelling, DAX calculations and dashboard development.

## 11. Final Outcome

The data preparation process reduced the dataset from 35 columns to 32 columns while retaining all 1,470 employee records.

The original dataset was preserved, unnecessary constant columns were removed from the analytical copy, and potential outliers were investigated rather than automatically deleted.

The resulting dataset was used as the foundation for the HR Employee Attrition Analysis dashboard.
