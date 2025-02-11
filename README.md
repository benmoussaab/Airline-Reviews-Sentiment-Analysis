# Airline-Reviews-Sentiment-Analysis

This repository contains a sentiment analysis project for airline reviews, developed as an application from my last Coursera course on machine learning.

## 📌 Project Overview

The goal of this project is to analyze airline customer reviews and classify them into sentiment categories (e.g., positive, neutral, or negative). It was just a bit application for my last coursera course

## 📊 Dataset

The dataset consists of airline reviews collected from passengers. It includes:
- Customer reviews (text)
- Sentiment labels (Positive, Neutral, Negative)
- Additional metadata (e.g., airline name, date, rating)

## 🛠️ Technologies Used

- **Python**: Data processing and modeling
- **Pandas**: Data manipulation
- **Scikit-learn**: Machine learning models
- **NLTK / spaCy**: Text preprocessing
- **Jupyter Notebook**: Code development

## 🔄 Preprocessing Steps

1. **Text Cleaning**: Removing punctuation, special characters, and stopwords.
2. **Tokenization & Lemmatization**: Converting text into structured tokens.
3. **Vectorization**: Converting text into numerical representations (TF-IDF or Word2Vec).
4. **Data Splitting**: Training and test set separation.

## 📈 Model Training

Different machine learning models are trained to classify sentiment, including:
- Logistic Regression
- XGBoost
- Deep Learning

## 📈 Model Evaluation

- I used AUC


## 🚀 How to Run the Project

1. Clone this repository:
   ```sh
   git clone https://github.com/your-username/airline-sentiment-analysis.git
   cd airline-sentiment-analysis
