# Sentiment Analysis

This project uses Natural Language Processing (NLP) and Machine Learning to classify tweets into Positive, Negative, and Neutral sentiments.

## Objective

The objective of this project is to analyse text data and build machine learning models that can automatically classify the sentiment of tweets.

## Tools and Technologies Used

- Python
- Pandas
- Scikit-learn
- NLTK
- Matplotlib
- Seaborn
- WordCloud
- Jupyter Notebook

## Dataset

The dataset contains Twitter posts and sentiment labels.

The main columns used in this project are:

- OriginalTweet
- Sentiment

The original dataset contained five sentiment categories:

- Negative
- Extremely Negative
- Neutral
- Positive
- Extremely Positive

For this project, the extreme sentiment categories were combined:

- Extremely Negative → Negative
- Extremely Positive → Positive

The final sentiment distribution was:

- Negative: 1,633
- Positive: 1,546
- Neutral: 619

## Data Preprocessing

The following text preprocessing steps were performed:

- Converted text to lowercase
- Removed punctuation and special characters
- Tokenised text
- Removed English stopwords
- Created cleaned tweet text for model training

## Feature Extraction

TF-IDF Vectorizer was used to convert the cleaned text into numerical features.

The feature matrix contained:

- 3,798 tweets
- 5,000 features

## Train-Test Split

The dataset was divided using an 80/20 split:

- Training data: 3,038 tweets
- Testing data: 760 tweets

## Machine Learning Models

Two machine learning classifiers were trained and evaluated:

### 1. Multinomial Naive Bayes

Results:

- Accuracy: 61.45%
- Precision: 67.92%
- Recall: 61.45%
- F1-Score: 55.95%

### 2. Logistic Regression

Results:

- Accuracy: 68.42%
- Precision: 71.23%
- Recall: 68.42%
- F1-Score: 66.16%

## Model Comparison

| Model | Accuracy | Precision | Recall | F1-Score |
|-------|----------|-----------|--------|----------|
| Naive Bayes | 61.45% | 67.92% | 61.45% | 55.95% |
| Logistic Regression | 68.42% | 71.23% | 68.42% | 66.16% |

## Visualisations

The following visualisations were created:

- Sentiment distribution bar chart
- Confusion matrix for Naive Bayes
- Confusion matrix for Logistic Regression
- Negative sentiment word cloud
- Positive sentiment word cloud
- Neutral sentiment word cloud

## Error Analysis

Examples of misclassified tweets were analysed to understand possible reasons for incorrect predictions.

Misclassifications can occur because:

- Tweets may contain ambiguous language
- Context may be difficult for the model to understand
- Sarcasm and informal language can affect predictions
- Short tweets may not contain enough information
- Some sentiment labels may be subjective

## Conclusion

Both models were successfully trained to classify tweet sentiment. Logistic Regression performed better than Naive Bayes across all major evaluation metrics.

The Logistic Regression model achieved the highest accuracy of **68.42%** and an F1-score of **66.16%**.

This type of sentiment analysis can be used for:

- Customer feedback analysis
- Social media monitoring
- Brand reputation analysis
- Public opinion analysis
- Product review analysis

The project demonstrates how Natural Language Processing and Machine Learning can be combined to automatically analyse and classify opinions expressed in text.
