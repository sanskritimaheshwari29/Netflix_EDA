# 🎬 Netflix Movies & TV Shows – Exploratory Data Analysis

A Python-based Exploratory Data Analysis (EDA) project on the Netflix
Titles dataset to understand patterns, trends, content distribution,
and other insights from Netflix's movies and TV shows.

## 📌 Project Overview

This project explores the Netflix Titles dataset using Python.
The dataset was cleaned, analyzed, and visualized to understand
the type of content available on Netflix and identify important
patterns and trends.

## 🎯 Objectives

- Understand the Netflix dataset
- Perform basic data cleaning and preprocessing
- Check duplicate records
- Analyze Movies and TV Shows
- Analyze content by country
- Analyze the most common genres
- Analyze content ratings
- Analyze content released over the years
- Generate meaningful insights using visualizations

## 📊 Dataset

**Netflix Titles Dataset**

The dataset contains information about movies and TV shows available
on Netflix.

### Key Columns

- title
- type
- director
- cast
- country
- date_added
- release_year
- rating
- duration
- listed_in
- description

## 🛠️ Tools & Technologies

- Python
- Pandas
- Matplotlib
- Google Colab

## 🔍 Analysis Performed

### 1. Data Loading and Understanding
- Loaded the Netflix dataset using Pandas
- Examined the structure and basic information of the dataset

### 2. Data Cleaning
- Checked for duplicate records
- Converted the `date_added` column into datetime format

### 3. Content Type Analysis
Analyzed the distribution of Movies and TV Shows.

- Movies: 6,131
- TV Shows: 2,676

### 4. Country Analysis
Analyzed the countries contributing the most Netflix titles.

Top countries included:
- United States
- India
- United Kingdom
- Japan
- South Korea
- Canada
- Spain
- France
- Mexico

### 5. Genre Analysis
Identified the Top 10 most common genre combinations using
the `listed_in` column.

### 6. Rating Analysis
Analyzed the Top 10 most common content ratings.

The most common ratings included:
- TV-MA
- TV-14
- TV-PG
- R
- PG-13
- TV-Y7
- TV-Y
- PG
- TV-G
- NR

### 7. Release Year Analysis
Analyzed the number of Netflix titles released across different years
using a line chart.

## 📈 Visualizations

The project includes visualizations for:

- Top 10 Most Common Genres
- Top 10 Most Common Ratings
- Content Released per Year
- Country-wise content distribution

## 📌 Key Findings

- Movies are more numerous than TV Shows in the dataset.
- The United States has the highest number of titles among the listed countries.
- `TV-MA` is the most common content rating.
- Drama and International Movies is one of the most common genre combinations.
- Netflix content increased significantly in the later years of the dataset.
- The dataset contains a wide variety of movies and TV shows across different countries and genres.

## 💡 Conclusion

The Netflix EDA project provides an overview of the content available
on Netflix by analyzing content type, country, genre, ratings, and
release years.

The analysis shows that Netflix has a larger number of Movies than
TV Shows, with the United States being the leading country in terms
of titles. The visualizations also show the growth of Netflix content
over the years and highlight the most common ratings and genres.

This project helped in understanding how Python, Pandas, and Matplotlib
can be used for data cleaning, exploratory analysis, and visualization.

## 📂 Project Structure

Netflix_EDA/
│
├── Final_Netflix_EDA_Project.ipynb
├── README.md
├── .gitignore
└── .gitattributes

## ▶️ How to Run

1. Clone or download this repository.
2. Open `Final_Netflix_EDA_Project.ipynb` in Google Colab.
3. Upload the Netflix dataset if required.
4. Run the notebook cells sequentially.
