# 🎬 Netflix Movies & TV Shows — Exploratory Data Analysis

## 📌 Project Overview

This project performs an **Advanced Exploratory Data Analysis (EDA)** on the Netflix Movies & TV Shows dataset using Python.

The analysis explores Netflix's content catalog from different perspectives, including:

* Content type distribution
* Country-wise content distribution
* Genre analysis
* Content ratings
* Release-year trends
* Movie duration
* Missing values and data quality
* Relationships between content type, country and ratings
* Correlation and outlier analysis

The project uses statistical analysis and visualizations to identify meaningful patterns in the Netflix catalog.

---

## 📊 Dataset

The analysis is performed on the **Netflix Movies & TV Shows dataset**.

### Dataset Size

* **Rows:** 8,807
* **Columns:** 12
* **Numerical Columns:** 1
* **Categorical/Object Columns:** 11

### Main Columns

| Column         | Description                                 |
| -------------- | ------------------------------------------- |
| `show_id`      | Unique ID of the title                      |
| `type`         | Movie or TV Show                            |
| `title`        | Title name                                  |
| `director`     | Director of the title                       |
| `cast`         | Cast members                                |
| `country`      | Country/countries associated with the title |
| `date_added`   | Date added to Netflix                       |
| `release_year` | Original release year                       |
| `rating`       | Content rating                              |
| `duration`     | Movie duration or number of seasons         |
| `listed_in`    | Genres/categories                           |
| `description`  | Description of the title                    |

---

## 🛠️ Technologies & Libraries

* **Python**
* **Pandas** — Data manipulation and analysis
* **NumPy** — Numerical operations
* **Matplotlib** — Data visualization
* **Seaborn** — Statistical visualization
* **Jupyter Notebook / Google Colab**

---

## 🔍 Project Workflow

### 1. Data Loading

The dataset is loaded using Pandas and the initial records are examined.

```python
df = pd.read_csv('netflix_titles.csv')
```

The dataset contains **8,807 records and 12 columns**.

---

### 2. Dataset Exploration

The notebook examines:

* Dataset dimensions
* Data types
* Statistical summary
* Numerical and categorical columns
* Number of unique values
* Initial records

The `release_year` column ranges from **1925 to 2021**.

---

### 3. Data Quality Assessment

Missing values and duplicate records were investigated.

The major missing values were found in:

| Column     | Missing Values |
| ---------- | -------------: |
| Director   |          2,634 |
| Country    |            831 |
| Cast       |            825 |
| Date Added |             10 |
| Rating     |              4 |
| Duration   |              3 |

No duplicate rows were found.

Missing values in `director`, `cast`, and `country` were handled by replacing them with **"Unknown"**.

The notebook also identified **3 records where duration values were incorrectly present in the rating column** and corrected them.

`date_added` was converted to a proper datetime format for further analysis.

---

## 📈 Exploratory Data Analysis

### Univariate Analysis

The notebook analyzes individual variables such as:

* Movies vs TV Shows
* Top countries
* Top genres
* Content ratings

### Content Type

The dataset contains:

* **6,131 Movies**
* **2,676 TV Shows**

This represents approximately:

* **69.62% Movies**
* **30.38% TV Shows**

### 🌎 Top Countries

Based on title counts, the leading countries include:

1. United States
2. India
3. United Kingdom
4. Canada
5. France
6. Japan
7. Spain
8. South Korea
9. Germany

The analysis also separates multiple countries listed in a single record using `explode()`.

### 🎭 Top Genres

The most frequently occurring genres/categories include:

1. International Movies
2. Dramas
3. Comedies
4. International TV Shows
5. Documentaries
6. Action & Adventure
7. TV Dramas
8. Independent Movies
9. Children & Family Movies
10. Romantic Movies

### 🔞 Content Ratings

The most common ratings include:

* TV-MA
* TV-14
* TV-PG
* R
* PG-13

---

## 🔄 Bivariate Analysis

The project examines relationships between pairs of variables.

### Analysis Performed

* Movies vs TV Shows across top countries
* Rating distribution by content type
* Release-year trends
* Release-year distribution
* Movie-duration distribution

Visualizations include:

* Bar charts
* Heatmaps
* Line charts
* Histograms
* Box plots

---

## 🧩 Multivariate Analysis

Multiple variables are analyzed together to identify deeper patterns.

The notebook examines:

* Country + Content Type + Rating
* Genre + Content Type
* Release Year + Movie Duration

A correlation matrix was created for movie release year and duration.

The observed correlation between **release year and movie duration is approximately -0.21**, indicating a weak negative relationship in this dataset.

---

## 📐 Advanced Statistical Analysis

### Movie Duration

Movie durations were converted from text such as `90 min` into numerical values.

Key statistics:

| Statistic |     Value |
| --------- | --------: |
| Count     |     6,128 |
| Mean      | 99.58 min |
| Median    |    98 min |
| Q1        |    87 min |
| Q3        |   114 min |
| Maximum   |   312 min |

### IQR-Based Outlier Detection

The notebook calculates:

* Q1 = 87 minutes
* Q3 = 114 minutes
* IQR = 27 minutes
* Lower Bound = 46.5 minutes
* Upper Bound = 154.5 minutes

Using these boundaries, **450 potential movie-duration outliers** were identified.

These are treated as potential statistical outliers and are not automatically assumed to be errors.

---

## 📊 Visualizations

The project includes visualizations such as:

* Netflix content type distribution
* Missing-value percentage
* Top countries by number of titles
* Top genres
* Content rating distribution
* Movies vs TV Shows across countries
* Rating heatmap
* Release-year trend
* Release-year histogram
* Movie-duration box plot
* Movie-duration histogram
* Genre contribution
* Correlation heatmap
* IQR-based outlier visualization

---

## 💡 Key Insights

Some important observations from the analysis are:

* Movies form the majority of the Netflix catalog in the dataset.
* The United States has the highest number of associated titles.
* India is among the major contributors to the Netflix catalog.
* International Movies and Dramas are highly represented genres.
* TV-MA is the most frequent content rating.
* Netflix content is heavily concentrated in more recent release years, particularly around 2016–2020.
* Movie durations are generally concentrated around approximately 1.5–2 hours.
* The dataset contains substantial missing information, especially for directors.
* Movie duration contains several statistical outliers based on the IQR method.

---

## 📁 Project Structure

```text
Netflix-EDA/
│
├── Netflix_EDA.ipynb
├── netflix_titles.csv
└── README.md
```

> If the dataset is not included in the repository, the notebook can be run after placing `netflix_titles.csv` in the appropriate working directory.

---

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone <your-repository-url>
```

### 2. Install required libraries

```bash
pip install pandas numpy matplotlib seaborn
```

### 3. Open the notebook

You can run the notebook using:

* Jupyter Notebook
* JupyterLab
* Google Colab

### 4. Load the dataset

Make sure `netflix_titles.csv` is available at the path used in the notebook.

### 5. Run the notebook

Execute the cells sequentially to reproduce the analysis and visualizations.

---

## 🎯 Learning Outcomes

Through this project, the following data-analysis skills were applied:

* Data loading and inspection
* Data cleaning
* Missing-value handling
* Duplicate detection
* Feature transformation
* Datetime conversion
* Categorical analysis
* Frequency analysis
* Data visualization
* Univariate analysis
* Bivariate analysis
* Multivariate analysis
* Descriptive statistics
* Correlation analysis
* IQR-based outlier detection
* Exploratory data analysis

---

## 🏁 Conclusion

This project provides a comprehensive exploratory analysis of the Netflix Movies & TV Shows dataset.

By combining **data cleaning, statistical analysis and visualization**, the project identifies patterns in Netflix's content type, genres, ratings, countries, release years and movie durations.

The analysis demonstrates how Python-based EDA can be used to transform a raw entertainment dataset into meaningful insights and visual findings.

---

## 👩‍💻 Author

**Sanskriti Maheshwari**

### Skills Demonstrated

`Python` · `Pandas` · `NumPy` · `Matplotlib` · `Seaborn` · `Data Cleaning` · `EDA` · `Data Visualization` · `Statistics`
