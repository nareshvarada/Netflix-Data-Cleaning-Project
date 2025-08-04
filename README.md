# Netflix-Data-Cleaning-Project
A Python-based data cleaning project for a raw Netflix titles dataset. This repository demonstrates a complete data cleaning workflow using pandas to handle missing values, duplicates, and inconsistent data formats. It includes the original data, the cleaning script, and the final cleaned CSV file.

I have successfully cleaned the netflix_titles.csv dataset.
Here is a summary of the changes I made:

Missing Values:

13 rows were removed due to missing values in the date_added or duration columns.

Missing values in the director, cast, country, and rating columns were filled with 'Unknown'.

Duplicates: No duplicate rows were found in the dataset.

Column Headers: All column names were converted to lowercase and spaces were replaced with underscores for consistency (e.g., release_year).

Data Types:

The date_added column was converted from an object to a datetime object.

The duration column, which contained values like "90 min" or "2 Seasons", was split into two new columns: duration_value (numeric) and duration_unit (text). The original duration column was then dropped.
Netflix Data Cleaning Project
This repository documents a data cleaning and preparation project for a dataset of Netflix titles. The primary objective was to take a raw, messy dataset and transform it into a clean, usable format suitable for analysis.

Objective
The goal of this project was to clean and prepare the netflix_titles.csv dataset, which contained common data issues such as missing values, inconsistent formats, and unstructured columns.

Tools Used
Python: The core programming language used for the project.

Pandas: A powerful Python library used for data manipulation and analysis.

Cleaning Process
The data cleaning process followed these steps:

Initial Inspection: The dataset was loaded and an initial inspection was performed using df.info() and df.isnull().sum() to identify missing values, data types, and overall structure.

Handling Missing Values:

Rows with missing date_added or duration values were dropped as they were critical for the analysis.

Missing values in the director, cast, country, and rating columns were filled with the string 'Unknown'.

Removing Duplicates: The dataset was checked for duplicate rows, but none were found.

Standardizing Column Headers: All column names were converted to lowercase and spaces were replaced with underscores (e.g., release year became release_year).

Data Type Conversion and Transformation:

The date_added column, initially a string, was converted to a proper datetime object for time-series analysis.

The duration column was split into two new columns, duration_value (an integer) and duration_unit (a string), to separate the numeric value from the unit (e.g., 'min', 'Seasons'). The original duration column was then dropped.

This process resulted in a clean, structured dataset ready for further exploration and analysis. The cleaned data can be found in cleaned_netflix_titles.csv, and the full cleaning script is available in data_cleaning_script.py.
