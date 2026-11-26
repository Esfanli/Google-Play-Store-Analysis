# 📱 Google Play Store Data Analysis

**Author:** [ESfanli] | **GitHub:** [@Esfanli](https://github.com/Esfanli)

---

This project performs an in-depth Exploratory Data Analysis (EDA) on the Google Play Store dataset. The goal is to clean, process, and visualize the data to uncover patterns in app ratings, popular categories, pricing strategies, and user engagement.

## 🛠 Tech Stack & Libraries
* **Language:** Python
* **Data Manipulation:** `pandas`, `numpy`
* **Data Visualization:** `matplotlib`, `seaborn`
* **Text Processing:** `re` (Regular Expressions)

## 📂 Dataset Overview
The dataset (`googleplaystore.csv`) contains information on 10,840 applications across 13 columns, including:
* `App`: Application name
* `Category`: App category
* `Rating`: User rating
* `Reviews`: Number of user reviews
* `Size`: App size
* `Installs`: Number of installs
* `Type`: Free or Paid
* `Price`: App price
* `Content Rating`: Age rating
* `Genres`: App genres
* `Last Updated`, `Current Ver`, `Android Ver`: Metadata

## ⚙️ Data Preprocessing
Before visualization, the raw data underwent several cleaning steps:
1. **Data Cleaning:** Removed invalid records (e.g., the `'Life Made WI-FI Touchscreen Photo Frame'` anomaly) and reset the index.
2. **Handling Missing Values & Data Types:** Analyzed missing values (e.g., 9,659 null values in the `Rating` column) using `df.info()` and `df.describe()`.
3. **Type Conversion (Casting):**
   * Converted `Reviews` from string to `int64`.
   * Cleaned and converted `Size` to `float64` (handling 'M' and 'k' suffixes).
   * Removed special characters (+, ,) to convert `Installs` to `int64`.
   * Removed the '$' sign to convert `Price` to `float64`.
   * Extracted a new `Main_Genre` column from the `Genres` column.

## 📊 Visualizations & Insights
The notebook includes four main visualizations:

1. **Rating Distribution:** A histogram with a KDE curve showing that the majority of apps are rated between **4.0 and 4.5**.
2. **Top 10 Categories:** A bar chart revealing that categories like **FAMILY**, **GAME**, and **TOOLS** have the highest number of applications.
3. **Free vs. Paid Apps Rating Comparison:** A boxplot showing that while the median rating for both groups is similar, paid apps have more low-rating outliers.
4. **Reviews vs. Rating Relationship:** A scatter plot with a logarithmic X-axis demonstrating that apps with a massive number of reviews (100k+) tend to have highly concentrated, high ratings.

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/Esfanli/Google-Play-Store-Analysis.git
