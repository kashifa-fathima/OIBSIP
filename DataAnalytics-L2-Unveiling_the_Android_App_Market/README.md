# OIBSIP – Task 4: Unveiling the Android App Market

## Google Play Store Analysis

### 📌 Project Overview

This project focuses on analyzing the Google Play Store to understand application trends, categories, ratings, installations, pricing, estimated revenue, and user sentiment.

The project uses two datasets:

1. Google Play Store Apps Dataset
2. Google Play Store User Reviews Dataset

The analysis includes data cleaning, exploratory data analysis, visualization, revenue estimation, and sentiment analysis of user reviews.

---

## 🎯 Objective

The main objective of this project is to perform a comprehensive analysis of the Google Play Store and identify useful insights that can help developers understand the app market and make better decisions when planning a new application.

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- TextBlob
- Plotly
- Jupyter Notebook / Google Colab

---

## 📂 Datasets

### 1. Google Play Store Apps Dataset

Contains information about applications available on the Google Play Store, including:

- App
- Category
- Rating
- Reviews
- Size
- Installs
- Type
- Price
- Content Rating
- Genres
- Last Updated
- Current Version
- Android Version

### 2. Google Play Store User Reviews Dataset

Contains user reviews and sentiment-related information, including:

- App
- Translated Review
- Sentiment
- Sentiment Polarity
- Sentiment Subjectivity

---

## 🔍 Project Workflow

### 1. Data Loading

Both datasets were loaded separately using Pandas.

### 2. Data Exploration

The datasets were explored using:

- `head()`
- `shape`
- `columns`
- `info()`
- `describe()`
- Missing-value analysis
- Duplicate-value analysis

### 3. Data Cleaning

The following cleaning operations were performed:

- Removed duplicate applications
- Converted the `Installs` column into numerical values
- Removed special characters such as `+` and `,` from installation values
- Converted `Price` into numerical values
- Removed `$` symbols from prices
- Converted application size into MB
- Handled `Varies with device` values
- Handled missing ratings using the median
- Handled missing values in relevant categorical columns
- Checked and removed duplicate records

After cleaning, the applications dataset contained approximately:

**9,660 applications and 15 columns**, including the derived analysis columns.

---

## 📊 Exploratory Data Analysis

### Category Analysis

The number of applications in each category was analyzed using bar charts.

This helped identify:

- Most common app categories
- Categories with fewer applications
- Potentially saturated categories

### ⭐ Ratings Analysis

The distribution of application ratings was visualized using histograms.

Average ratings were also calculated for different categories to compare application quality across categories.

### 📱 Size vs Installs

A scatter plot was created to analyze the relationship between application size and number of installations.

Correlation analysis was also performed to understand whether application size has a meaningful relationship with installations.

### 💰 Pricing Analysis

Applications were divided into:

- Free
- Paid

The distribution of free and paid applications was visualized.

For paid applications, the price distribution was also analyzed.

### 💵 Estimated Revenue

An estimated revenue metric was created using:

`Estimated Revenue = Installs × Price`

Revenue was aggregated by category to identify categories with higher estimated revenue potential.

> Note: This is only an estimated revenue proxy. It does not represent actual developer earnings because factors such as refunds, taxes, platform fees, promotional pricing, and actual purchase conversions are not included.

---

## 💬 Sentiment Analysis

User reviews were analyzed using **TextBlob**.

Each review was classified into one of three sentiment categories:

- Positive
- Negative
- Neutral

The sentiment distribution was visualized to understand the overall user response to applications.

Sentiment was also analyzed by application category to identify categories receiving comparatively more positive or negative feedback.

---

## 📈 Visualizations

The project includes visualizations such as:

- App distribution by category
- Rating distribution
- Average rating by category
- App size vs installations
- Free vs paid application distribution
- Paid application price distribution
- Estimated revenue by category
- Overall sentiment distribution
- Sentiment by category
- Interactive Plotly visualization

---

## 💡 Key Insights

### 1. Free Applications Dominate

Free applications make up the majority of applications available in the dataset, indicating that free distribution is a common strategy for reaching a larger user base.

### 2. Competition Varies Across Categories

Some categories contain significantly more applications than others. Categories with a large number of applications may represent highly competitive and saturated markets.

### 3. User Sentiment Can Guide Development

Sentiment analysis of reviews provides useful information about user satisfaction. Positive reviews can highlight successful features, while negative reviews can help developers identify areas that need improvement.

---

## 📌 Business Recommendations

Based on the analysis, a developer planning a new application should:

1. Research category competition before launching an application.
2. Consider a free or freemium strategy to maximize user acquisition.
3. Monitor ratings and reviews regularly.
4. Use negative feedback to identify and improve application weaknesses.
5. Study successful categories and applications before deciding on a target market.
6. Consider both user demand and market saturation when selecting an app category.
