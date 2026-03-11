# Sentiment Analysis on IMDB Movie Reviews

## Overview

This project builds a binary sentiment classifier for IMDB movie reviews (positive vs. negative). We start by implementing Bag-of-Words and TF-IDF from scratch, then run systematic experiments with sklearn pipelines to find the best model configuration.

## Methods

- Implemented BoW and TF-IDF by hand to understand the mechanics
- Compared 24 combinations of vocabulary size, n-gram range, and classifier (Naive Bayes, Logistic Regression, Linear SVM)
- Analyzed the best model with feature weights and error analysis
- Built an n-gram language model as a generative extension

## Key Results

- Best model: TF-IDF (1,2) + Linear SVM + 20,000 features — 88.2% test accuracy
- Bigrams helped (+1.2 points); going beyond bigrams gave no further gain
- Main failure modes: sarcasm, negation, and mixed sentiment

## How to Run

1. Install dependencies: `pip install -r requirements.txt`
2. Open the notebook: `jupyter notebook notebooks/main_analysis.ipynb`
3. Run all cells in order. The IMDB dataset (~80 MB) will download automatically on first run.

## Requirements

See `requirements.txt`. Python 3.9+ required.