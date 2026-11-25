# Data Quality Assessment Report

## 1. Project Overview

This report documents the data quality assessment performed on the IBM HR Employee Attrition dataset before data cleaning and preparation.

The purpose of this assessment was to understand the dataset structure, identify potential data quality issues, validate values and determine whether the dataset was suitable for further analysis.

### Dataset Overview

| Attribute | Details |
|---|---|
| Dataset | IBM HR Employee Attrition |
| Total Records | 1,470 |
| Total Columns | 35 |
| Tools Used | Python, Pandas, Jupyter Notebook |

## 2. Data Structure and Type Assessment

The original dataset contained the following data types:

| Data Type | Number of Columns |
|---|---:|
| Integer (`int64`) | 26 |
| String (`object`) | 9 |
| **Total** | **35** |

Data types were inspected to understand the structure of the dataset and identify columns requiring special consideration.

EmployeeNumber was treated as an employee identifier rather than a numerical measure. Ordinal-coded columns, such as Education and JobSatisfaction, were recognised as categorical values with an inherent order.

## 3. Missing Value Assessment

All columns were checked for missing values.

| Assessment | Result |
|---|---:|
| Total Missing Values | 0 |
| Columns with Missing Values | 0 |

**Finding:** No missing values were identified in the original dataset. Therefore, no missing-value treatment was required.

## 4. Duplicate Assessment

The dataset was checked for duplicate records and duplicate employee identifiers.

| Assessment | Result |
|---|---:|
| Duplicate Rows | 0 |
| Duplicate EmployeeNumber Values | 0 |

**Finding:** No duplicate records or duplicate employee identifiers were identified.

## 5. Categorical Data Assessment

Categorical columns were examined using frequency distributions to understand the employee population and identify unexpected category values.

### Key Category Distributions

**Attrition**

| Category | Employee Count |
|---|---:|
| No | 1,233 |
| Yes | 237 |

**Department**

| Category | Employee Count |
|---|---:|
| Research & Development | 961 |
| Sales | 446 |
| Human Resources | 63 |

**Gender**

| Category | Employee Count |
|---|---:|
| Male | 882 |
| Female | 588 |

**Business Travel**

| Category | Employee Count |
|---|---:|
| Travel_Rarely | 1,043 |
| Travel_Frequently | 277 |
| Non-Travel | 150 |

The remaining categorical columns, including EducationField, JobRole, MaritalStatus and OverTime, were also examined.

## 6. Numerical Data Assessment

Numerical columns were inspected using descriptive statistics, including minimum, maximum, mean, median, quartiles and standard deviation.

### Selected Numerical Ranges

| Column | Minimum | Maximum |
|---|---:|---:|
| Age | 18 | 60 |
| DistanceFromHome | 1 | 29 |
| TotalWorkingYears | 0 | 40 |
| YearsAtCompany | 0 | 40 |
| YearsInCurrentRole | 0 | 18 |
| YearsSinceLastPromotion | 0 | 15 |
| YearsWithCurrManager | 0 | 17 |
| MonthlyIncome | 1,009 | 19,999 |

**Finding:** The numerical ranges were reviewed to identify unusual values and support further validation.

## 7. Constant Column Assessment

Columns containing only one unique value were identified.

| Column | Constant Value |
|---|---|
| EmployeeCount | 1 |
| Over18 | Y |
| StandardHours | 80 |

**Finding:** Three constant columns were identified. These columns contained no variation and were considered unnecessary for the intended analysis.

## 8. Outlier Assessment

The Interquartile Range (IQR) method was used to identify potential statistical outliers in selected numerical columns.

### Outlier Results

| Column | Potential Outliers |
|---|---:|
| Age | 0 |
| TotalWorkingYears | 63 |
| MonthlyIncome | 114 |
| YearsAtCompany | 104 |
| DistanceFromHome | 0 |

### Investigation and Decisions

- **Age:** No potential outliers were identified.
- **TotalWorkingYears:** Potential outliers were investigated in relation to employee age, company tenure and job roles.
- **MonthlyIncome:** Potential outliers were examined in relation to job roles. Higher income values were observed among senior positions, including Managers and Research Directors.

**Decision:** Potential statistical outliers were not automatically classified as errors or removed. The investigated values were retained because they could represent legitimate employee characteristics.

## 9. Business Rule Validation

The following checks were performed to identify potential inconsistencies:

| Validation Check | Purpose |
|---|---|
| Age range | Check values against an assumed general range of 18–65 |
| MonthlyIncome | Check for positive income values |
| TotalWorkingYears vs YearsAtCompany | Check career experience against current company tenure |
| YearsInCurrentRole vs YearsAtCompany | Check role tenure against company tenure |
| YearsWithCurrManager vs YearsAtCompany | Check manager tenure against company tenure |
| EmployeeNumber | Verify employee identifier uniqueness |

**Note:** The age range of 18–65 was used as a general validation assumption, not as a confirmed company policy.

These checks were used to investigate potential inconsistencies rather than automatically modify employee records.

## 10. Text and Ordinal Value Validation

Text columns were checked for:

- Leading and trailing spaces.
- Inconsistent capitalization.
- Unexpected category values.

Ordinal-coded columns were checked against their expected value ranges. These included:

- Education
- EnvironmentSatisfaction
- JobInvolvement
- JobLevel
- JobSatisfaction
- PerformanceRating
- RelationshipSatisfaction
- StockOptionLevel
- WorkLifeBalance

**Finding:** No unexpected text category values or ordinal codes were identified during the validation checks.

## 11. Initial Data Quality Summary

| Quality Check | Result |
|---|---:|
| Original Records | 1,470 |
| Original Columns | 35 |
| Missing Values | 0 |
| Duplicate Rows | 0 |
| Duplicate EmployeeNumber Values | 0 |
| Constant Columns | 3 |
| Age IQR Outliers | 0 |
| TotalWorkingYears IQR Outliers | 63 |
| MonthlyIncome IQR Outliers | 114 |

## 12. Conclusion

The initial assessment found that the IBM HR Employee Attrition dataset contained no missing values or duplicate records.

Three constant columns were identified, and potential outliers were investigated using the IQR method. Business rule checks, categorical assessments and ordinal value validations were also performed.

The assessment provided the foundation for the subsequent data cleaning and preparation process.

The original dataset was preserved, and cleaning operations were performed on a separate copy to maintain the integrity of the source data.
