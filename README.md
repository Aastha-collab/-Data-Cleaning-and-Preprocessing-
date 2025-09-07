# DataCleaning and Preprocessing
Netflix Dataset Cleaning and Standardization using Excel.

## **Project Overview**

This project focuses on cleaning and preparing the Netflix dataset for data analysis. The objective was to ensure that the data is consistent, standardized, and formatted properly to support meaningful insights. The dataset contains information on Netflix’s movies and TV shows, including details like title, cast, country, date added, rating, duration, and more.

All tasks were completed by following data cleaning best practices using **Excel**, including handling missing values, removing duplicates, standardizing data, and correcting data types.

---

##  **Step-by-Step Process**

### 1️. **Checked for Missing Values**

* Used the **Filter tool** to inspect each column for blank or missing values.
* Counted how many empty cells exist in every columnn using excel formula =COUNTBLANK(clean_table[show_id])
* Verified that missing data is minimal or explained

Column     | Missing Before | Action Taken                      | Missing After
-----------|----------------|-----------------------------------|--------------
director   | 369            | Replaced blanks with 'Unknown'    | 0
cast       | 825            | Replaced blanks with 'Not Listed' | 0
country    | 830            | Replaced blanks with 'Unknown'    | 0
date_added | 10             | Filled with Jan-01-release_year   | 0
rating     | 4              | Replaced with 'Unrated'           | 0
duration   | 3              | Replaced with 'Unknown'           | 0

---

### 2️. **Removed Duplicate Rows**

* Checked for duplicates using **Data → Remove Duplicates** based on the `show_id` column.
* Confirmed that `show_id` is unique for every record.
* No duplicate rows were found, so the dataset integrity is maintained.
* Then we checked for 'title, type, release_year' and found 4 duplicates and removed from the dataset. 
---

### 3️. **Standardized Text Values**

* Inspected columns like `country`, `rating`, and `listed_in` for inconsistent naming.
* Trimmed extra spaces using the **TRIM function** to ensure consistency.
* Confirmed that all categorical columns now follow a clean and uniform structure.

---

### 4️. **Converted Dates into a Consistent Format**

* Applied **Format Cells → Date → dd-mm-yyyy** to the `date_added` column.
* Used **Text to Columns** to ensure all date values were recognized as date types rather than text.
* Verified that the `release_year` column contains only numeric values and requires no modification.

---

### 5️. **Renamed Columns to Be Clean and Uniform**

* Verified that all column headers are already:

  * Lowercase
  * Without spaces (underscores used instead)
  * Descriptive and consistent
    - No changes were required in this step.

---

### 6️. **Checked and Fixed Data Types**

* Ensured:

  * `show_id` is treated as an integer.
  * `release_year` is numeric.
  * `date_added` is in date format.
  * `duration` column  includes both minutes and seasons.

---

##  **Tools Used**

* Microsoft Excel (Filters, Text to Columns, Data Validation, Remove Duplicates)
* Formulas: `TRIM`, `LEFT`, `RIGHT`, `VALUE`, `FIND`
* Format Cells → Date options

---

##  **Conclusion**

The Netflix dataset is now clean, standardized, and ready for analysis. All missing values, duplicates, inconsistent text entries, and improper data types have been handled. The dataset can now be used to extract insights such as:

* Popular genres per country
* Trends by date added
* Analysis based on duration types
* Audience preferences across regions
