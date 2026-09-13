# House Price Prediction using Linear Regression

## Oasis Infobyte Data Analytics Internship — Task 1

This project focuses on predicting house prices using **Linear Regression**. The dataset contains different property characteristics such as area, number of bedrooms, bathrooms, floors, year built, location, condition, and garage availability.

The project covers the complete machine learning workflow, starting from data exploration and preprocessing to model training and evaluation.

---

## Objective

The objective of this project is to build a Linear Regression model that can predict house prices based on available property features.

---

## Dataset

The dataset used for this project is:

**House Price Prediction Dataset.csv**

### Dataset Features

| Feature | Description |
|---|---|
| Id | Unique property identifier |
| Area | Area of the house |
| Bedrooms | Number of bedrooms |
| Bathrooms | Number of bathrooms |
| Floors | Number of floors |
| YearBuilt | Year the house was built |
| Location | Location category |
| Condition | Condition of the property |
| Garage | Garage availability |
| Price | Target variable — house price |

The `Id` column was excluded from model training because it is only an identifier and does not provide meaningful information about house prices.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## Project Workflow

### 1. Data Loading

The dataset was loaded using Pandas and its structure, shape, columns, and data types were examined.

### 2. Exploratory Data Analysis

The dataset was analyzed using:

- Dataset shape
- Data types
- Missing-value analysis
- Descriptive statistics
- House price distribution
- Correlation analysis
- Categorical feature analysis

### 3. Feature Selection

The following features were selected as predictors:

- Area
- Bedrooms
- Bathrooms
- Floors
- YearBuilt
- Location
- Condition
- Garage

The target variable is:

- Price

The `Id` column was excluded because it is an identifier.

### 4. Data Preprocessing

Categorical features were converted into numerical representations using **One-Hot Encoding**.

The preprocessing and model training were implemented using a Scikit-learn Pipeline.

### 5. Train-Test Split

The dataset was divided into:

- **80% Training Data**
- **20% Testing Data**

A `random_state` of 42 was used to ensure reproducibility.

### 6. Model

A **Linear Regression** model from Scikit-learn was trained using the processed features.

### 7. Model Evaluation

The model was evaluated using:

- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score

### 8. Visual Analysis

The project includes:

- House Price Distribution
- Correlation Heatmap
- Actual vs Predicted Price Plot
- Residual Plot

---

## Model Results

The Linear Regression model produced the following results:

| Metric | Result |
|---|---:|
| MSE | 78,321,466,146.03 |
| RMSE | 279,859.73 |
| R² Score | -0.0067 |

### Interpretation

The model achieved a negative R² score, indicating that the Linear Regression model provides limited predictive performance on this dataset.

The numerical features showed very weak linear correlations with the target variable, Price. The Actual vs Predicted plot also showed that the predicted values were concentrated around the average price instead of closely following the actual prices.

The residual plot showed a wide spread of residuals around the zero line, which is consistent with the model's weak predictive performance.

These results highlight the importance of having meaningful relationships between input features and the target variable when developing a machine learning model.

---

## Key Learnings

Through this project, I gained practical experience in:

- Loading and exploring datasets using Pandas
- Performing Exploratory Data Analysis
- Checking and handling missing values
- Selecting relevant features
- Encoding categorical variables
- Splitting data into training and testing sets
- Building a Linear Regression model
- Using Scikit-learn Pipelines
- Evaluating regression models
- Interpreting MSE, RMSE, and R²
- Creating data visualizations using Matplotlib and Seaborn
- Performing residual analysis
- Understanding model limitations

