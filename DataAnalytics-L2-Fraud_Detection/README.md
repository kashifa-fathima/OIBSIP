L2 Task3

# Fraud Detection

## 📌 Project Overview

This project focuses on detecting fraudulent credit card transactions using machine learning.

Fraud detection is a challenging classification problem because fraudulent transactions are extremely rare compared with legitimate transactions. Therefore, this project focuses not only on model training but also on handling class imbalance and evaluating models using appropriate fraud-detection metrics.

---

## 🎯 Objective

The main objectives of this project are:

* Analyze the class imbalance in financial transactions.
* Perform Exploratory Data Analysis (EDA).
* Compare transaction amounts for fraudulent and legitimate transactions.
* Analyze fraud patterns by time of day.
* Explain why accuracy is misleading for highly imbalanced datasets.
* Handle class imbalance using SMOTE.
* Train and compare multiple machine learning models.
* Evaluate models using Precision, Recall, F1-Score, and ROC-AUC.
* Analyze feature importance.
* Discuss the Precision-Recall trade-off.
* Consider how the fraud detection system could scale to high transaction volumes.

---

## 📊 Dataset

The project uses the **Credit Card Fraud Detection** dataset.

### Dataset Information

* Total Transactions: **284,807**
* Legitimate Transactions: **284,315**
* Fraudulent Transactions: **492**
* Fraud Rate: **approximately 0.173%**
* Total Features: **30**
* Target Variable: `Class`

### Target Variable

| Class | Meaning                |
| ----- | ---------------------- |
| 0     | Legitimate Transaction |
| 1     | Fraudulent Transaction |

The dataset contains anonymized features `V1` to `V28`, which are PCA-transformed variables. Therefore, these features do not have direct human-readable business meanings.

> **Note:** The original dataset is not included in this repository due to dataset redistribution considerations. The notebook can be run after placing `creditcard.csv` in the project directory.

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Imbalanced-learn
* SMOTE
* Matplotlib
* Seaborn
* Jupyter Notebook / Google Colab

---

## 🔄 Project Workflow

The project follows these major steps:

1. Import required libraries
2. Load the dataset
3. Inspect the dataset
4. Analyze class imbalance
5. Perform Exploratory Data Analysis
6. Analyze transaction amounts
7. Analyze fraud by time of day
8. Explain why accuracy is misleading
9. Prepare features and target
10. Perform stratified train-test split
11. Scale the features
12. Apply SMOTE to the training data
13. Train Logistic Regression
14. Train Random Forest
15. Evaluate both models
16. Plot the ROC-AUC curves
17. Analyze feature importance
18. Discuss Precision vs Recall
19. Discuss scalability
20. Draw conclusions

---

## ⚠️ Class Imbalance

The dataset is highly imbalanced.

Only approximately **0.173%** of transactions are fraudulent.

This means that a model could achieve very high accuracy by predicting almost every transaction as legitimate while failing to detect actual fraud.

Therefore, accuracy alone is not an appropriate metric for evaluating this problem.

---

## 📈 Exploratory Data Analysis

The following analyses were performed:

### Transaction Amount Analysis

Transaction amounts were compared between fraudulent and legitimate transactions to identify differences in their distributions.

### Time-of-Day Analysis

The `Time` feature was converted into an hour-based representation to investigate whether fraudulent transactions showed different patterns during different hours of the day.

---

## ⚖️ Handling Class Imbalance — SMOTE

SMOTE (Synthetic Minority Over-sampling Technique) was used to address the severe class imbalance.

SMOTE creates synthetic examples of the minority class instead of simply duplicating existing fraud cases.

Importantly, SMOTE was applied **only to the training data** after the train-test split. This prevents information from the test set from leaking into the training process.

---

## 🤖 Machine Learning Models

Two classification models were trained:

### 1. Logistic Regression

Logistic Regression was used as a baseline classification model.

It provides a relatively simple and interpretable approach for binary classification.

### 2. Random Forest

Random Forest was used as a more powerful tree-based ensemble model.

It combines multiple decision trees to improve predictive performance and provides feature importance values that can be used to understand which features contributed most to predictions.

---

## 📏 Evaluation Metrics

Because the dataset is highly imbalanced, the following metrics were used:

### Precision

Measures how many transactions predicted as fraudulent were actually fraudulent.

### Recall

Measures how many of the actual fraudulent transactions were successfully detected.

### F1-Score

Provides a balance between Precision and Recall.

### ROC-AUC

Measures the model's ability to distinguish between fraudulent and legitimate transactions across different classification thresholds.

---

## 📊 Model Results

Replace the values below with the actual results from your notebook:

| Model               |  Precision |     Recall |   F1-Score |    ROC-AUC |
| ------------------- | ---------: | ---------: | ---------: | ---------: |
| Logistic Regression | Add result | Add result | Add result | Add result |
| Random Forest       | Add result | Add result | Add result | Add result |

The model comparison was performed using fraud-specific evaluation metrics rather than accuracy alone.

---

## 🔍 Feature Importance

Feature importance was analyzed using the Random Forest model.

The top features were identified based on their contribution to the model's predictions.

Since `V1` to `V28` are anonymized PCA-transformed features, their importance indicates predictive contribution rather than a directly interpretable business factor.

---

## 🎯 Recall vs Precision

For fraud detection, **Recall is particularly important** because missed fraudulent transactions can result in financial losses.

However, maximizing Recall alone may result in more legitimate transactions being incorrectly flagged as fraudulent.

Therefore, a practical fraud detection system needs to find an appropriate balance between:

* **High Recall** → Detect more fraud.
* **High Precision** → Reduce false fraud alerts.
* **High F1-Score** → Maintain a balance between Precision and Recall.

The appropriate balance depends on the business cost of missed fraud versus false alerts.

---

## 🚀 Scalability

The task also considers a scenario involving approximately **1 million transactions per hour**, which is around 278 transactions per second.

For such a high-volume environment, the fraud detection system could be scaled using:

* Efficient feature preprocessing
* Parallel prediction
* Batch or real-time processing
* Multiple model-serving instances
* Distributed data-processing systems
* Continuous model monitoring
* Periodic model retraining
* Fraud-pattern and concept-drift monitoring

A production system would also need to maintain low prediction latency while processing a large number of transactions.


---

## ✅ Key Learnings

Through this project, I learned:

* How to work with highly imbalanced datasets.
* Why accuracy can be misleading in fraud detection.
* How to use stratified train-test splitting.
* How to apply SMOTE correctly.
* How to train classification models.
* How to evaluate models using Precision, Recall, F1-Score, and ROC-AUC.
* How to interpret feature importance.
* How to analyze the Precision-Recall trade-off.
* How machine learning systems can be designed for large-scale transaction processing.

---

## 🏁 Conclusion

This project demonstrated an end-to-end machine learning approach for detecting fraudulent financial transactions.

The major challenge was the extreme class imbalance, with fraudulent transactions representing only approximately 0.173% of the dataset. SMOTE was therefore used on the training data to improve the representation of the minority class.

Logistic Regression and Random Forest were trained and evaluated using fraud-focused metrics including Precision, Recall, F1-Score, and ROC-AUC. The project also examined feature importance, the Precision-Recall trade-off, and the scalability requirements of a high-volume fraud detection system.

Overall, the project provided practical experience in handling imbalanced classification problems and designing a machine learning workflow for a real-world fraud detection scenario.

---

## 👩‍💻 Author

**Kashifa Fathima**

**Track:** Data Analytics
**Project:** Fraud Detection
**Internship:** Oasis Infobyte (OIBSIP)
