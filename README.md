# elevate-lab-task-1-data-analysis

# 🎬 Netflix Movies & TV Shows

## Data Cleaning and Preprocessing Project



Project Overview

This project focuses on cleaning and preprocessing the **Netflix Movies and TV Shows dataset** to make it analysis-ready.

Raw datasets often contain:

* Missing values
* Duplicate records
* Inconsistent text formats
* Incorrect data types
* Unstructured column names

The goal of this project is to transform raw data into a **clean, structured, and reliable dataset** suitable for further analysis or visualization.

# Objective

To clean and standardize the Netflix dataset by:

* Handling missing values
* Removing duplicate rows
* Standardizing text values
* Converting date formats
* Renaming column headers
* Fixing incorrect data types


 🛠 Tools Used

* 🐍 Python
* 📊 Pandas
* Jupyter Notebook


📂 Dataset

Dataset used: Netflix Movies and TV Shows Dataset

* Title
* Director
* Cast
* Country
* Release Year
* Rating
* Duration
* Genre
* Date Added



 🧹 Data Cleaning Steps Performed

1️⃣ Handling Missing Values

* Identified null values using:

python
df.isnull().sum()


* Filled missing categorical fields where appropriate.
* Left some fields as NaN when data was genuinely unavailable.
* Removed rows where critical information was missing.

---

2️⃣ Removing Duplicate Records

Checked for duplicate rows:

python
df.duplicated().sum()


Removed duplicates:

python
df.drop_duplicates(inplace=True)

 3️⃣ Standardizing Text Values

* Converted text columns to lowercase
* Removed leading/trailing spaces
* Standardized country names
* Cleaned inconsistent genre formatting

Example:

python
df['country'] = df['country'].str.strip().str.lower()


 4️⃣ Converting Date Format

Converted `date_added` column to datetime format:

python
df['date_added'] = pd.to_datetime(df['date_added'])


Ensured consistent date format across the dataset.

5️⃣ Renaming Columns

Standardized column names:

* Lowercase
* Removed spaces
* Replaced spaces with underscores

Example:

python
df.columns = df.columns.str.lower().str.replace(" ", "_")


6️⃣ Fixing Data Types

Verified and corrected data types:

python
df.dtypes


* `release_year` → Integer
* `date_added` → Datetime
* Text fields → String

 ✅ Final Cleaned Dataset

After preprocessing:

* No duplicate rows
* Reduced missing values
* Consistent formatting
* Correct data types
* Clean column naming

The cleaned dataset is ready for:

* Exploratory Data Analysis (EDA)
* Data Visualization
* Dashboard creation (Power BI / Tableau)
* Machine Learning models


 📊 Before vs After Summary

| Issue             | Before Cleaning             | After Cleaning        |
| ----------------- | --------------------------- | --------------------- |
| Missing Values    | Present in multiple columns | Handled               |
| Duplicate Records | Found                       | Removed               |
| Inconsistent Text | Yes                         | Standardized          |
| Date Format       | Mixed/Raw                   | Converted to datetime |
| Column Names      | Unclean                     | Standardized          |


📁 Project Structure


📦 Netflix-Data-Cleaning
 ┣ 📜 netflix_raw.csv
 ┣ 📜 netflix_cleaned.csv
 ┣ 📓 data_cleaning.ipynb
 ┗ 📜 README.md






 📈 Future Improvements

* Perform Exploratory Data Analysis
* Create Power BI dashboard
* Build recommendation system
* Perform genre-based trend analysis



