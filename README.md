# Sentiment Analysis of Product Reviews using NLP

![Python](https://img.shields.io/badge/Python-3.x-blue) ![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-green) ![NLP](https://img.shields.io/badge/NLP-sentiment-purple)

A Natural Language Processing project that classifies product reviews as **Positive**, **Negative**, or **Neutral** using text preprocessing and Logistic Regression in Python.

## Overview

This project builds a complete NLP pipeline — from raw text to a trained sentiment classifier. It demonstrates core NLP concepts including text cleaning, tokenization, stopword removal, feature extraction (Bag of Words and TF-IDF), and machine learning classification.

## Features

- Full text preprocessing pipeline (lowercase, punctuation removal, tokenization, stopword removal)
- Two feature extraction methods: Bag of Words and TF-IDF Vectorization
- Logistic Regression classifier trained on both feature sets
- Model evaluation using Accuracy, Precision, Recall, and F1-Score
- Predict sentiment on new, unseen product reviews

## Tech Stack

| Library | Purpose |
|---|---|
| `scikit-learn` | ML model, vectorizers, evaluation |
| `pandas` | Dataset management |
| `numpy` | Numerical operations |
| `re` | Regular expressions for text cleaning |

## Project Structure

```
sentiment-analysis-nlp/
├── sentiment_analysis.py   # Main script (full pipeline)
├── README.md               # This file
└── requirements.txt        # Dependencies
```

## How It Works

### 1. Dataset
75 manually labelled product reviews — 25 Positive, 25 Negative, 25 Neutral — split 70/30 into training and test sets.

### 2. Preprocessing
```
Input  : "This product is AMAZING and very useful!"
Output : "product amazing useful"
```

### 3. Feature Extraction
Each cleaned review is converted into a numerical vector using CountVectorizer (BoW) and TfidfVectorizer.

### 4. Model Training & Results

| Model | Features | Accuracy |
|---|---|---|
| Logistic Regression | Bag of Words | ~57% |
| Logistic Regression | TF-IDF | ~52% |

## Getting Started

```bash
# 1. Clone the repo
git clone https://github.com/your-username/sentiment-analysis-nlp.git
cd sentiment-analysis-nlp

# 2. Install dependencies
pip install scikit-learn pandas numpy

# 3. Run the project
python sentiment_analysis.py
```

## Sample Output

```
Review                                           Predicted Sentiment
---------------------------------------------------------------
This is the best product I have ever bought!    Positive
Completely useless, broke on the first day      Negative
It is fine, nothing special about it            Neutral
Fantastic quality and very fast shipping        Positive
Disappointed with the overall build quality     Negative
```

## Author

Haseeb — Computer Science student. Built as part of an AI/NLP course assignment.
