L2 Task 2

# 🍷 Wine Quality Prediction

## 📌 Project Overview

This project focuses on predicting wine quality using machine learning classification algorithms based on the physicochemical properties of red wine.

The project was completed as **Task 2 – Wine Quality Prediction** as part of the **Data Analytics Internship at Oasis Infobyte**.

Three classification models were trained and compared:

* Random Forest Classifier
* Stochastic Gradient Descent (SGD) Classifier
* Support Vector Classifier (SVC)

The models were evaluated using accuracy, precision, recall, F1-score, and confusion matrices.

---

## 🎯 Objective

The main objectives of this project are to:

* Explore and understand the Wine Quality dataset.
* Analyze the distribution of wine quality scores.
* Perform exploratory data analysis on physicochemical properties.
* Identify relationships between chemical properties and wine quality.
* Analyze class imbalance in the original quality scores.
* Convert the original quality scores into three practical categories.
* Train and compare three classification algorithms.
* Identify important features using Random Forest.
* Determine the most suitable model for predicting wine quality categories.

---

## 📊 Dataset

The project uses the **Wine Quality – Red Wine** dataset.

The dataset contains physicochemical measurements of red wine samples along with their quality scores.

### Features

* Fixed Acidity
* Volatile Acidity
* Citric Acid
* Residual Sugar
* Chlorides
* Free Sulfur Dioxide
* Total Sulfur Dioxide
* Density
* pH
* Sulphates
* Alcohol

### Target

The original target variable is:

`quality`

The quality score ranges from low to high values, with most observations concentrated around the middle quality scores.

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook / Google Colab

### Machine Learning Algorithms

* Random Forest Classifier
* SGD Classifier
* Support Vector Classifier (SVC)

---

## 🔍 Project Workflow

### 1. Data Loading and Inspection

The dataset was loaded using Pandas and inspected to understand:

* Dataset dimensions
* Column names
* Data types
* Statistical summary
* Missing values
* Duplicate records
* Quality-score distribution

### 2. Exploratory Data Analysis

EDA was performed using:

* Quality distribution plots
* Feature distribution plots
* Correlation analysis
* Correlation heatmap

The analysis helped identify patterns and relationships among the physicochemical properties.

### 3. Class Imbalance Analysis

The original quality scores were not evenly distributed. Some quality scores contained significantly more observations than others.

This imbalance can cause classification models to favor the majority classes and perform poorly on underrepresented classes.

---

## ⚙️ Feature Engineering

To make the classification problem more practical and reduce the effect of sparse individual quality scores, the original quality scores were grouped into three categories:

| Quality Score | Category |
| ------------- | -------- |
| 3–4           | Low      |
| 5–6           | Medium   |
| 7–8           | High     |

The model predicts these three categories instead of the individual quality scores.

This approach retains more information than a simple binary Good/Bad classification.

---

## 🧪 Model Training

The dataset was divided into training and testing sets using an **80:20 split**.

Stratified sampling was used to maintain similar class proportions in both datasets.

Feature scaling was applied for the SGD and SVC models using `StandardScaler`.

### Models

#### Random Forest

A Random Forest Classifier was trained using the original numerical features.

#### SGD Classifier

A Stochastic Gradient Descent Classifier was trained using standardized features.

#### SVC

A Support Vector Classifier with an RBF kernel was trained using standardized features.

---

## 📈 Model Evaluation

The models were evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix

### Model Comparison

| Model          |         Accuracy | Weighted F1-Score |
| -------------- | ---------------: | ----------------: |
| Random Forest  | **[Add result]** |  **[Add result]** |
| SGD Classifier | **[Add result]** |  **[Add result]** |
| SVC            | **[Add result]** |  **[Add result]** |

The model with the strongest overall performance based on the evaluation metrics was selected as the preferred model.

---

## 📊 Confusion Matrix

Confusion matrices were created for all three models to understand how well each classifier distinguished between:

* Low
* Medium
* High

quality wines.

The confusion matrices also helped identify which quality categories were most frequently misclassified.

---

## 🌟 Feature Importance

Feature importance was extracted from the Random Forest model to identify the physicochemical properties that contributed most to the classification.

The feature-importance visualization helps understand which chemical characteristics were most useful for predicting wine quality categories.

---

## 🏆 Conclusion

This project demonstrated how machine learning classification techniques can be used to predict wine quality categories from physicochemical properties.

The original quality scores were converted into **Low, Medium, and High** categories to create a more practical three-class classification problem.

Random Forest, SGD Classifier, and SVC were trained and evaluated using the same train-test framework.

Based on the final evaluation results, **[Best Model]** achieved the strongest overall performance with an accuracy of **[Accuracy]** and a weighted F1-score of **[F1-Score]**.

Therefore, **[Best Model]** is considered the most suitable model for deployment among the three tested approaches.

The project also showed the importance of exploratory data analysis, class-imbalance analysis, feature scaling, and appropriate evaluation metrics when developing classification models.

---

## ▶️ How to Run

### 1. Clone the repository

```bash
git clone <your-OIBSIP-repository-link>
```

### 2. Open the project folder

```bash
cd DataAnalytics-Task2-WineQualityPrediction
```

### 3. Install required libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### 4. Open the notebook

```bash
jupyter notebook Wine_Quality_Prediction.ipynb
```

Alternatively, upload the notebook and dataset to **Google Colab** and run the cells sequentially.

---

## 📌 Key Takeaways

* Wine quality is influenced by multiple physicochemical properties.
* The original quality scores are imbalanced.
* Grouping the scores into three categories makes the classification task more practical.
* Stratified splitting helps preserve class proportions.
* Feature scaling is important for models such as SGD and SVC.
* Different classification algorithms can produce different results on the same dataset.
* Random Forest feature importance provides useful insight into the variables contributing to predictions.


