# 🎬 Correlation Analysis in Python

This project explores and visualizes correlations in a movie dataset using Python libraries such as **pandas**, **seaborn**, and **matplotlib**. It focuses on understanding the relationships between different features like budget, gross revenue, score, and votes.

---

## 📁 Dataset

The dataset used is a CSV file containing movie details such as:
- Title
- Budget
- Gross Earnings
- Runtime
- Score
- Votes
- Company
- Country
- Released Year

> 📌 **Location**: `movies.csv` (placed locally in `C:\dev\PythonProject\Correlation in python\movies.csv`)

> **Source**: https://www.kaggle.com/datasets/danielgrijalvas/movies/data

---

## 🔧 What This Project Does

### 1. **Data Loading and Display**
- Reads the CSV file into a pandas DataFrame.
- Provides a scrollable output for viewing large DataFrames using HTML.

### 2. **Handling Missing Data**
- Displays columns and rows with missing values.
- Fills missing numeric values using:
  - Manual imputation for small numbers of missing rows.
  - Median values grouped by `score_range` (for `budget` and `gross`).
- Fills missing categorical values with `'Unknown'`.
- Drops rows with severe missing data if needed.

### 3. **Data Cleaning**
- Converts data types to proper formats (`int64` for `budget` and `gross`).
- Extracts the correct year from the `released` column.
- Removes duplicates.

### 4. **Visualization**
- Scatter plot and regression plot between `budget` and `gross`.
- Heatmap showing correlation matrix between all numeric features.

### 5. **Correlation Analysis**
- Computes correlation using:
  - Pearson (default)
  - Spearman (for ranked/ordinal data)
- Converts categorical (object) columns to numeric using `.cat.codes`.
- Sorts correlation pairs to find the strongest positive relationships.
- Outputs:
  - Correlation matrix
  - Top correlation pairs
  - Highest correlations (above 0.5)

---

## 📈 Key Insight

> 🎯 **Budget and Gross Earnings** show the highest correlation — suggesting that a higher budget generally leads to higher earnings.

---

## 📚 Libraries Used

- `pandas`
- `numpy`
- `seaborn`
- `matplotlib`
- `IPython.display` (for scrollable DataFrame display)

---

## 💻 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/Correlation_python.git
