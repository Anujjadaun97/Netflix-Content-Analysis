# Netflix Content Analysis 📺

## Project Overview

This project analyzes the Netflix Movies and TV Shows dataset to uncover insights into content distribution, genre popularity, country contributions, content growth trends, and duration patterns. The goal is to understand Netflix's content strategy and identify key characteristics of its catalog through Exploratory Data Analysis (EDA) and data visualization.

---

## Dataset

**Source:** Netflix Movies and TV Shows Dataset (Kaggle)

**Dataset Size:**

* Total Records: 8,807
* Total Columns: 12

### Features Included

* Show ID
* Type (Movie / TV Show)
* Title
* Director
* Cast
* Country
* Date Added
* Release Year
* Rating
* Duration
* Genre (listed_in)
* Description

---

## Project Objectives

The analysis focused on answering the following business questions:

1. What is the distribution of Movies and TV Shows on Netflix?
2. Which countries contribute the most content?
3. How has Netflix's content library evolved over time?
4. Which genres are most popular?
5. What are the duration patterns of Movies and TV Shows?
6. How do international co-productions impact country contributions?

---

## Data Cleaning & Preparation

### Data Quality Checks

* Checked dataset structure and data types.
* Identified missing values.
* Checked duplicate records and duplicate titles.
* Investigated inconsistent values.

### Key Cleaning Steps

* Converted `date_added` from object to datetime format.
* Extracted:

  * Added Year
  * Added Month
  * Added Day
* Corrected misplaced duration values stored in the rating column.
* Extracted:

  * Duration Value
  * Duration Type
* Split multi-country entries for advanced country contribution analysis.
* Split multi-genre entries for genre popularity analysis.

---

## Missing Values Summary

| Column     | Missing Values |
| ---------- | -------------: |
| Director   |          2,634 |
| Cast       |            825 |
| Country    |            831 |
| Date Added |             10 |
| Rating     |              4 |
| Duration   |              3 |

No duplicate records or duplicate titles were found.

---

# Key Findings

---

## 1. Movie vs TV Show Analysis

### Distribution

| Content Type | Count | Percentage |
| ------------ | ----: | ---------: |
| Movie        | 6,131 |     69.62% |
| TV Show      | 2,676 |     30.38% |

### Insights

* Movies dominate Netflix's catalog, accounting for nearly 70% of all content.
* The movie library is approximately 2.3 times larger than the TV Show library.
* Netflix has historically maintained a stronger focus on movies than episodic content.

---

## 2. Country Contribution Analysis

### Top Contributing Countries (Original Data)

| Country        | Titles |
| -------------- | -----: |
| United States  |  2,818 |
| India          |    972 |
| United Kingdom |    419 |
| Japan          |    245 |
| South Korea    |    199 |

### Insights

* The United States is the largest contributor to Netflix's catalog.
* India is the second-largest contributor, highlighting the importance of Indian entertainment content.
* Netflix's content library spans multiple continents, reflecting global diversification.

---

## 3. Advanced Country Analysis (Co-Productions)

### Problem

Approximately 16.55% of records contained multiple countries.

Example:

```text
United States, Canada
United Kingdom, United States
India, United States
```

### Solution

Countries were split and counted individually to properly account for co-productions.

### Top Contributors After Splitting Co-Productions

| Country        | Titles |
| -------------- | -----: |
| United States  |  3,690 |
| India          |  1,046 |
| United Kingdom |    806 |
| Canada         |    445 |
| France         |    393 |

### Insights

* The United States remained the dominant contributor after accounting for co-productions.
* The United Kingdom, Canada, and France experienced significant increases in contribution counts.
* Germany entered the Top 10 after co-production analysis, demonstrating the importance of international collaborations.
* Ignoring co-productions significantly understates the contribution of several countries.

---

## 4. Content Release Trend Analysis

### Key Statistics

* Oldest Content: 1925
* Latest Content: 2021
* Average Release Year: 2014
* Median Release Year: 2017

### Peak Content Year

| Year | Titles |
| ---- | -----: |
| 2018 |  1,147 |

### Insights

* Netflix's catalog is heavily concentrated in recent years.
* Content growth accelerated rapidly after 2015.
* 2018 was the peak release year in the dataset.
* Content production remained strong between 2017 and 2020.
* A decline appears in 2021, likely due to dataset limitations or incomplete yearly data.

---

## 5. Genre Popularity Analysis

### Top Genres

| Genre                  | Count |
| ---------------------- | ----: |
| International Movies   | 2,752 |
| Dramas                 | 2,427 |
| Comedies               | 1,674 |
| International TV Shows | 1,351 |
| Documentaries          |   869 |

### Insights

* International Movies are the most common genre on Netflix.
* Drama and Comedy are among the most popular content categories.
* International content dominates both Movies and TV Shows.
* Netflix strongly emphasizes globally produced content.

---

## 6. Duration Analysis

### Movie Duration Statistics

| Metric           |        Value |
| ---------------- | -----------: |
| Average Duration | 99.6 Minutes |
| Median Duration  |   98 Minutes |
| Maximum Duration |  312 Minutes |

### Insights

* Most movies are between 80 and 120 minutes long.
* The average Netflix movie duration is approximately 100 minutes.
* Extremely long movies are rare.

---

### TV Show Duration Statistics

| Metric          | Value |
| --------------- | ----: |
| Average Seasons |  1.76 |
| Median Seasons  |     1 |
| Maximum Seasons |    17 |

### Insights

* Most TV Shows have only one season.
* The majority of TV Shows contain 1–2 seasons.
* Long-running series are relatively uncommon on Netflix.

---

# Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Jupyter Notebook / Google Colab

---

# Visualizations Created

* Movie vs TV Show Distribution
* Country Contribution Analysis
* Country Co-Production Analysis
* Release Year Trend Analysis
* Genre Popularity Analysis
* Movie Duration Distribution
* TV Show Season Distribution

---

# Conclusion

This analysis reveals that Netflix's content library is heavily movie-oriented, internationally diverse, and strongly focused on modern content. International Movies emerged as the most popular genre, while the United States remains the largest contributor to the platform's catalog. Advanced co-production analysis demonstrated the importance of international collaborations, significantly increasing the contributions of countries such as the United Kingdom, Canada, and France.

The findings highlight Netflix's global content acquisition strategy, emphasis on recent releases, and preference for shorter-form content consumption through feature-length movies and limited-series TV Shows.

---

## Author

**sTranGer**
Data Analysis Portfolio Project – Netflix Content Analysis
