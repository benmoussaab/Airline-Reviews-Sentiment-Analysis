# Airline Review Sentiment Analysis

A Natural Language Processing (NLP) project that predicts whether a passenger will recommend an airline based on their written review. 

## 📊 Overview
This project analyzes passenger flight reviews to classify them into "Recommended" (1) or "Not Recommended" (0)[cite: 1]. The dataset revealed a class imbalance, with only about 33.6% of the reviews resulting in a recommendation[cite: 1]. Various text vectorization techniques and machine learning models were built and compared to find the best performing predictive model.

## 🛠️ Tools & Technologies Used
* **Data Manipulation:** Pandas, NumPy[cite: 1]
* **Natural Language Processing (NLP):** NLTK (WordNetLemmatizer, stopwords, word_tokenize), Regular Expressions[cite: 1]
* **Machine Learning:** Scikit-Learn (Logistic Regression, CountVectorizer, TfidfVectorizer), XGBoost[cite: 1]
* **Evaluation Metrics:** ROC-AUC Score[cite: 1]
* **Visualizations:** Matplotlib, Seaborn, WordCloud *(added in final version)*

## 🚀 Project Pipeline

1. **Data Preprocessing:**
   * Mapped the "Recommended" target variable from "yes"/"no" strings to binary 1/0 integers[cite: 1].
   * Verified data integrity by checking for null values[cite: 1].

2. **Text Cleaning (NLP):**
   * Converted all text to lowercase[cite: 1].
   * Removed punctuation and extra whitespaces using RegEx[cite: 1].
   * Tokenized text and removed standard English stopwords[cite: 1].
   * Lemmatized words to their base forms using NLTK's WordNetLemmatizer[cite: 1].

3. **Feature Extraction & Modeling:**
   * **Model 1:** Logistic Regression using standard Bag of Words (`CountVectorizer`)[cite: 1].
   * **Model 2:** Logistic Regression using Term Frequency-Inverse Document Frequency (`TfidfVectorizer` with min_df=5)[cite: 1].
   * **Model 3:** Logistic Regression using N-Grams (1 to 3 words, min_df=5)[cite: 1].
   * **Model 4:** XGBoost Classifier using N-Gram features[cite: 1].

## 📈 Key Findings & Results
The models were evaluated using the Area Under the Receiver Operating Characteristic Curve (ROC-AUC) to account for the imbalanced classes. 

* **Logistic Regression (Base Bag of Words):** 0.876 AUC[cite: 1]
* **Logistic Regression (TF-IDF):** 0.883 AUC[cite: 1]
* **Logistic Regression (N-Grams 1-3):** **0.891 AUC** (Best Performing Model)[cite: 1]
* **XGBoost Classifier:** 0.878 AUC[cite: 1]

*Conclusion: The Logistic Regression model utilizing up to 3-word combinations (trigrams) captured the most context and performed the best at predicting airline recommendations.*

## ⚙️ How to Run
1. Clone this repository.
2. Ensure you have the required libraries installed (`pandas`, `numpy`, `nltk`, `scikit-learn`, `xgboost`, `matplotlib`, `seaborn`).
3. Download the necessary NLTK corpora by running the first few cells of the notebook.
4. Run `kkl.ipynb` in Jupyter Notebook or Jupyter Lab to view the end-to-end analysis.
