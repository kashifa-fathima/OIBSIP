# Autocomplete and Autocorrect Data Analytics

### 📌 Project Overview

This project focuses on analyzing and implementing basic **autocomplete and autocorrect systems** using Natural Language Processing (NLP) techniques.

A text corpus consisting of books from **Project Gutenberg** was used to build frequency-based language models. The project demonstrates text preprocessing, n-gram modeling, next-word prediction, spelling correction, evaluation metrics, and visualization.

---

## 🎯 Objectives

* Collect and prepare a large text corpus for NLP analysis.
* Perform text preprocessing including:

  * Lowercasing
  * Tokenization
  * Punctuation removal
  * Stopword removal
* Analyze word frequencies.
* Build a **Bigram-based autocomplete model**.
* Build a **Trigram-based autocomplete model**.
* Compare Bigram and Trigram autocomplete performance.
* Implement autocorrect using the `pyspellchecker` library.
* Evaluate autocorrect using deliberately misspelled words.
* Calculate accuracy, precision, and recall.
* Create visualizations for model performance.

---

## 📂 Dataset

The text corpus was collected from **Project Gutenberg**.

The following four books were used:

* `1342.txt` – *Pride and Prejudice*
* `11.txt` – *Alice's Adventures in Wonderland*
* `514.txt` – *Little Women*
* `1661.txt` – *The Adventures of Sherlock Holmes*

One additional file (`84.txt`) was not used because it could not be processed correctly.

The combined corpus was used for NLP preprocessing and n-gram generation.

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* NLTK
* Matplotlib
* Collections
* PySpellChecker
* Jupyter Notebook / Google Colab

---

## 🔄 Project Workflow

### 1. Data Collection

Multiple Project Gutenberg text files were loaded and combined into a single text corpus.

### 2. Text Preprocessing

The following preprocessing steps were performed:

1. Converted all text to lowercase.
2. Tokenized the text using NLTK.
3. Removed punctuation and non-alphabetic tokens.
4. Removed stopwords for frequency analysis.
5. Created a vocabulary from the processed text.

The vocabulary contained approximately **16,005 unique words** after stopword removal.

---

## 📊 Word Frequency Analysis

The frequency of words was calculated using Python's `Counter`.

The top 20 most frequent words were visualized using a bar chart.

Some of the most frequent words included:

* said
* one
* jo
* would
* little
* could
* much
* like
* see
* know

### Visualization

`top_20_frequent_words.png`

---

# ⌨️ Autocomplete

## Bigram Model

A Bigram model was created using pairs of consecutive words.

For example:

```text
"could not"
```

can be represented as:

```text
("could", "not")
```

The model predicts the next word based on the frequency of words that follow the given word.

The top 3 predictions were generated for 10 test inputs.

---

## Trigram Model

A Trigram model was created using three consecutive words.

For example:

```text
"could not be"
```

is represented as:

```text
("could", "not", "be")
```

The Trigram model uses two previous words as context to predict the next word.

This generally provides more contextual information than the Bigram model.

---

## 📈 Autocomplete Results

| Model   | Top-3 Accuracy | Precision@3 | Recall@3 |
| ------- | -------------: | ----------: | -------: |
| Bigram  |         70.00% |      23.33% |   70.00% |
| Trigram |        100.00% |      33.33% |  100.00% |

The Trigram model performed better on the selected test cases because it considers more contextual information.

### Visualization

`bigram_vs_trigram_accuracy.png`

`bigram_vs_trigram_performance.png`

---

# ✏️ Autocorrect

The `pyspellchecker` library was used to identify and correct spelling mistakes.

A test set containing **20 deliberately misspelled words** was created.

Examples include:

```text
recieve → receive
becuase → because
definately → definitely
seperate → separate
acheive → achieve
enviroment → environment
```

The system correctly corrected **19 out of 20** misspelled words.

---

## 📊 Autocorrect Results

| Metric    |  Score |
| --------- | -----: |
| Accuracy  | 95.00% |
| Precision | 95.00% |
| Recall    | 95.00% |

A second test set containing 20 correctly spelled words was also used as a control group. All 20 correctly spelled words remained unchanged.

### Confusion Matrix

`autocorrect_confusion_matrix.png`

The confusion matrix showed:

* True Positives: 19
* False Negatives: 1
* False Positives: 0
* True Negatives: 20

---

# 📌 Overall Results

| System               | Accuracy | Precision |  Recall |
| -------------------- | -------: | --------: | ------: |
| Bigram Autocomplete  |   70.00% |    23.33% |  70.00% |
| Trigram Autocomplete |  100.00% |    33.33% | 100.00% |
| Autocorrect          |   95.00% |    95.00% |  95.00% |

---

# 💡 Key Findings

* The **Trigram model outperformed the Bigram model** on the selected autocomplete test cases.
* Using two previous words provides more context for next-word prediction.
* The Bigram model achieved 70% Top-3 accuracy.
* The Trigram model achieved 100% Top-3 accuracy on the 10 selected test cases.
* The autocorrect system correctly handled 19 of the 20 deliberately misspelled words.
* All 20 correctly spelled control words were preserved.
* Frequency-based models are simple and easy to implement but have limitations when dealing with unseen or uncommon phrases.

---

# ⚠️ Limitations

* The autocomplete evaluation used only 10 test cases.
* The autocorrect evaluation used only 20 deliberately misspelled words.
* Frequency-based models depend heavily on the training corpus.
* Rare or unseen words may not receive useful predictions.
* The autocomplete model does not understand the deeper meaning or semantics of a sentence.
* The SpellChecker-based autocorrect system does not fully consider sentence context.
* The Project Gutenberg corpus contains historical writing styles and may not represent modern conversational language.
* Production systems such as smartphone keyboards use much larger datasets and more advanced contextual or neural language models.

---

# 🔮 Future Improvements

The project could be improved by:

* Using a larger and more diverse text corpus.
* Increasing the size of the test datasets.
* Adding sentence-level context.
* Implementing neural language models.
* Using word embeddings.
* Testing more advanced spelling correction algorithms.
* Adding personalization based on user typing patterns.
* Evaluating the models on real-world conversational text.

---

# 🏁 Conclusion

This project demonstrates the basic implementation and evaluation of **autocomplete and autocorrect systems using NLP**.

Two frequency-based autocomplete models, Bigram and Trigram, were developed and compared. The Trigram model achieved better performance because it uses additional contextual information when predicting the next word.

The autocorrect system achieved **95% accuracy, precision, and recall**, correctly correcting 19 of the 20 deliberately misspelled words while leaving all correctly spelled control
