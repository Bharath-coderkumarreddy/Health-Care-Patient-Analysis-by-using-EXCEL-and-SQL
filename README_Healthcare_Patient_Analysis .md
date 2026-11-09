# Healthcare Patient Analysis -- SQL, Excel & Dashboard

## Project Overview

This project focuses on cleaning and validating healthcare patient data
using **SQL**, then analyzing the data in **Excel** and presenting key
findings through an interactive dashboard.

The dashboard provides an overview of patient demographics, diagnoses,
treatments, admission trends, and billing information.

## Project Objectives

-   Clean and validate healthcare patient data using SQL.
-   Check data quality, including missing values and duplicate records.
-   Ensure columns use appropriate data types.
-   Analyze patient demographics, diagnoses, treatments, and billing.
-   Present key performance indicators (KPIs) and trends in a dashboard.

## Dataset

The project dashboard reports **940 total patients**.

The analysis includes fields and categories such as: - Patient ID and
patient demographics - Age, gender, and blood type - Diagnosis and
treatment - Admission and discharge dates - Total bill and prescription
details

## Tools and Technologies

-   **SQL / MySQL** -- data cleaning, querying, and validation
-   **Microsoft Excel** -- data review, analysis, and dashboard creation

## SQL Data Cleaning and Validation

SQL was used to prepare the healthcare dataset for analysis. The
workflow included:

1.  Inspecting table structure and records.
2.  Checking for missing or `NULL` values.
3.  Removing unwanted leading and trailing spaces using `TRIM()` where
    required.
4.  Checking for duplicate records and repeated patient IDs.
5.  Reviewing and correcting data types.
6.  Converting admission and discharge fields to the `DATE` data type
    where required.
7.  Validating the cleaned data before analysis.

Example SQL checks:

``` sql
-- Check the total number of records
SELECT COUNT(*) AS total_records
FROM patient_details;

-- Check for missing patient IDs
SELECT *
FROM patient_details
WHERE PatientID IS NULL;

-- Check for duplicate patient IDs
SELECT PatientID, COUNT(*) AS occurrences
FROM patient_details
GROUP BY PatientID
HAVING COUNT(*) > 1;
```

## Dashboard Highlights

### Key Performance Indicators

  KPI                    Dashboard Value
  -------------------- -----------------
  Total Patients                     940
  Total Bill               ₹94,36,534.95
  Average Total Bill          ₹10,038.87
  Average Age                50.35 years

### Patient Analysis

-   **Patients by gender:** Female -- 316, Male -- 318, Other -- 306.
-   **Patients by diagnosis:** Hypertension -- 187, Flu -- 178, Diabetes
    -- 197, Covid-19 -- 187, Asthma -- 191.
-   **Patients by treatment:** Medication -- 326, Surgery -- 289,
    Therapy -- 325.
-   **Patients by blood type:** A- -- 119, A+ -- 116, AB- -- 119, AB+ --
    127, B- -- 132, B+ -- 122, O- -- 114, O+ -- 91.
-   **Admission trend:** The dashboard displays patient admission trends
    for 2021, 2022, and 2023.

The gender, diagnosis, treatment, and blood-type category counts each
add up to 940 patients.

## Project Workflow

1.  Import the healthcare dataset into a SQL database.
2.  Inspect, clean, and validate the data using SQL.
3.  Review the cleaned data in Excel.
4.  Analyze patient and billing information.
5.  Build an interactive dashboard with KPI cards, charts, and slicers.

## Project Outcome

The project demonstrates how SQL can be used to clean and validate
healthcare data and how Excel can be used to analyze and communicate
insights. The dashboard summarizes 940 patients and provides an overview
of demographics, diagnoses, treatments, admission trends, and billing.

## Author

**Bharath Kumar Reddy**
