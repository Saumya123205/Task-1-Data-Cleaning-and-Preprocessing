# Netflix Dataset Cleaning and Preparation Project
<img width="220" height="300" alt="Netflix Dataset Cleaning Overview" src="https://github.com/user-attachments/assets/85dfb69d-49e5-40f4-8e5c-123d0a308f4d" />


## 📌 Project Overview
This project focuses on cleaning and preparing the Netflix dataset for analysis.
The raw dataset contained missing values, inconsistent formats, and unstructured columns.
Using Python (Pandas), we cleaned and transformed the data into a fully standardized, analysis-ready format.

##  The cleaned dataset can now be used for:

### 🔹 Trend analysis of Netflix movies and TV shows

### 🔹 Visualization of content growth over time

### 🔹 Insights into durations, seasons, and genres

### 🔹 Building machine learning models

## 🎯 Objective

### 🔹 Clean and structure the raw Netflix dataset.

### 🔹 Handle missing values and inconsistencies.

### 🔹 Standardize column names, date formats, and data types.

### 🔹 Create new useful features for analysis.

## 🛠 Tools & Libraries Used

### Python

### Pandas → For data cleaning and preprocessing

## Steps Followed
### 1. Load and Explore Dataset

#### 🔹 Loaded the dataset using Pandas.

#### 🔹 Checked basic information using .info(), .describe(), and .isnull() to understand structure and missing values.

### 2. Standardize Column Names

#### Converted all column names to lowercase and replaced spaces with underscores.

### 3. Handle Missing Values

#### 🔹 Filled missing categorical columns with placeholders:

#### ✅ director → "Unknown"

#### ✅ cast → "Unknown"

#### ✅ country → "Unknown"

#### ✅ rating → "Not Rated"

#### 🔹 Dropped rows where date_added or duration were missing since they are critical for time-based analysis.

### 4. Parse and Clean the Duration Column

#### The duration column contained two different formats:

#### ✅ Movies → "90 min"

#### ✅ TV Shows → "2 Seasons"

#### Created a custom function parse_duration() to split it into:

#### ✅ duration_minutes → For Movies

#### ✅ num_seasons → For TV Shows

#### ✅ Filled missing movie durations with the median duration.

#### ✅ Assigned num_seasons = 0 for movies.

### 5. Feature Engineering

#### 🔹 Converted date_added to datetime format.

#### Extracted:

#### ✅ year_added → Year when added to Netflix

#### ✅ month_added → Month when added to Netflix

### 6. Standardize Data Types

#### 🔹 Converted important columns to proper data types:

#### 🔹 release_year, year_added, month_added, num_seasons → Integer

### 7. Check for Duplicates

#### 🔹 Verified there were no duplicate rows in the dataset.

### 8. Final Clean Dataset

#### Exported the cleaned dataset as:

#### netflix_cleaned.csv

### The final dataset has:

#### 🔹 No missing values in critical fields

#### 🔹 Standardized and consistent formatting

#### 🔹 Ready for visualization and machine learning tasks

## 📊 Key Insights

### 🔹 Most Netflix movies are between 60–150 minutes long.

### 🔹 Most TV shows have 1–5 seasons, with very few having more than 8.

### 🔹 Significant growth in content additions post-2015.

## 🚀 Final Outcome

### 🔹 Raw Netflix dataset transformed into a clean, structured format.

### 🔹 Dataset now ready for EDA (Exploratory Data Analysis) and dashboard building.
