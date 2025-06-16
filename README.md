# IMDb Top 1000: Data Cleaning, Transformation & Enrichment

Author: Daniela de Sousa Silva

## Description

This project demonstrates a complete data wrangling pipeline using the IMDb Top 1000 Movies and TV Shows dataset. The goal was to clean, enrich, and prepare the data for potential downstream use in modeling (e.g., predicting box office revenue or audience reception).

## Project Scope

This notebook covers:
- Profiling and assessing data quality
- Cleaning inconsistent or malformed values
- Handling missing values via contextual imputation
- Outlier detection and transformation
- Feature engineering for enrichment and usability

The focus was on making decisions grounded in both technical logic and theoretical relevance to real-world media analytics.

## Tools Used

- **Python** (in Google Colab)
- `pandas`, `numpy` – data manipulation
- `matplotlib`, `seaborn` – visualization
- `collections.Counter` – frequency analysis

## Key Transformations

- **Dropped unnecessary columns**: e.g., poster link and overview text
- **Corrected invalid entries** (e.g., ‘PG’ mistakenly in release year)
- **Standardized names**: directors and actors
- **Created new variables**:
  - `Decade` (from year)
  - `Log_Votes` & `Log_Gross` for outlier handling
  - `Rating_Diff` (IMDb vs Metascore sentiment divergence)
  - `Avg_Star_Freq` (star prominence based on dataset frequency)
- **One-hot encoded genres** for modeling usability
- **Contextual imputation** for missing values (based on rating, decade, or genre)

## Outputs & Insights

- Distribution visualizations (IMDb ratings, gross revenue, etc.)
- Genre-based heatmap of average ratings per decade
- Correlation analysis of enriched variables
- Star frequency and its relationship with popularity and revenue

## File Contents

- `cleaned_imdb.csv`: final dataset
- `imdb_dataset_cleaning.ipynb`: full annotated notebook

## Author Notes

This project was done as part of a data science course with the intent of practicing real-world preprocessing on a complex, semi-structured dataset. While no model was built, all transformations were made with future modeling in mind.

## Dataset Source

IMDb Top 1000 Movies and TV Shows – [Kaggle](https://www.kaggle.com/datasets/harshitshankhdhar/imdb-dataset-of-top-1000-movies-and-tv-shows)

---
# 2025-06-16 Update: EDA

A new notebook, `imdb_eda.ipynb`, has been added as part of a follow-up assignment for the Explorative Data Analysis and Visualisation course.

## Purpose:

This notebook demonstrates core EDA techniques, including analysis of location, variance, distribution shape, covariance, correlation, and grouped comparisons, using the cleaned IMDb Top 1000 Movies dataset produced in the first project.

## Focus:

The EDA does not revisit data cleaning or enrichment, but instead builds on the cleaned dataset to extract analytical insights and support them with clear, well-annotated visualizations.

##	Key Content:

-	Boxplots and KDEs for univariate analysis
-	Correlation heatmap and scatter plots for bivariate exploration
-	Grouped comparisons by director and genre
-	All code is self-contained and produces reproducible visualizations

This extension highlights the value of a clean dataset for effective exploration and communication of data-driven insights.

## Note

The original notebook, `imdb_dataset_cleaning.ipynb`, and all previously included files remain unaltered. The new EDA notebook is fully independent and builds on the existing cleaned dataset without modifying any prior code or outputs.
