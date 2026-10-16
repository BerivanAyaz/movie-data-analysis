# 🎬 TMDB 5000 Movie Dataset - Exploratory Data Analysis & Preprocessing

This repository contains an end-to-end Exploratory Data Analysis (EDA) and Data Preprocessing pipeline performed on the popular **TMDB 5000 Movie Dataset** using Python. The project focuses on data cleaning strategies, handling missing values, correlation analysis, and feature engineering to derive actionable insights for movie production and revenue forecasting.

---

## 🚀 Project Overview
In the film industry, accurate budget planning and revenue prediction are crucial for maximizing Return on Investment (ROI). This notebook simulates real-world data science challenges by intentionally introducing missing data, cleaning it through robust statistical imputation, visualizing key relationships, and engineering new predictive features (such as ROI).

---

## 📊 Key Steps & Methodology

1. **Environment & Libraries Setup:**
   * Utilized core data analysis libraries: `Pandas`, `NumPy`, `Seaborn`, `Matplotlib`, and `ast`.
2. **Missing Data Simulation & Handling:**
   * Injected a 5% random missing value rate (`NaN`) to simulate real-world data imperfections.
   * Dropped highly sparse or irrelevant columns (`homepage`, `tagline`, `id`).
   * Imputed numerical columns using **Mean** (`runtime`, `vote_average`, `vote_count`) and **Median** (`budget`, `revenue`, `popularity`) to handle skewness.
   * Imputed categorical columns using the **Mode** and text columns (`title`, `overview`) with `"Unknown"` to maintain data integrity.
3. **Exploratory Data Analysis (EDA) & Visualization:**
   * Visualized distributions of numerical variables (Budgets, Popularity, Vote Averages) and categorical variables (Original Languages, Movie Status).
   * Analyzed correlation matrices using heatmaps to discover strong positive/negative relationships between budget, revenue, and vote counts.
4. **Feature Engineering:**
   * Extracted primary genres from JSON-like structured strings using `ast.literal_eval`.
   * Created a new financial metric: **ROI (Return on Investment)** calculated via `revenue / budget`.
   * Applied One-Hot Encoding to categorical features (`original_language`, `status`, `main_genre`) for future machine learning model readiness.
5. **Business Scenario & Model Proposal:**
   * Outlined a complete business case for a media company aiming to forecast movie revenues and optimize budget allocation using a **Random Forest Regressor**.

---

## 🛠️ Built With
* **Language:** Python 3.10+
* **Libraries:** Pandas, NumPy, Seaborn, Matplotlib
* **Environment:** Kaggle Notebooks / Jupyter Notebook

```text
├── movie-data-analysis.ipynb   # Main Jupyter Notebook containing the full analysis
└── README.md                   # Project documentation
