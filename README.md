# Spam Detection System using Machine Learning

## Overview
This project implements a Natural Language Processing (NLP) system to classify text messages as **Spam** or **Ham (Normal)**. The system applies multiple machine learning algorithms and compares their performance.

The goal is to build a robust spam detection model and provide a user-friendly interface for testing predictions.

---

## Project Objectives
- Preprocess and clean text data
- Extract meaningful features using TF-IDF
- Train and evaluate multiple machine learning models
- Compare model performance
- Build a simple GUI for user interaction

---

## Dataset
- Source: Kaggle Email Spam Dataset
- Records used: 100,000
- Features:
  - `body`: message text
  - `label`: classification (0 = Spam, 1 = Ham)

---

## Data Preprocessing
The following preprocessing steps were applied:

- Convert text to lowercase
- Remove URLs
- Remove numbers
- Remove special characters
- Remove extra whitespace

---

## Feature Extraction
TF-IDF vectorization was used to convert text into numerical features:

- ngram_range = (1, 3)
- max_df = 0.9
- min_df = 2
- max_features = 40000
- sublinear_tf = True

---

## Models Implemented

The following machine learning models were trained and evaluated:

1. Logistic Regression
2. Support Vector Machine (SVM)
3. Naive Bayes
4. Decision Tree Classifier
5. Random Forest Classifier

---

## Model Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score

### Performance Summary

| Model                  | Accuracy | Notes                                  |
|------------------------|----------|----------------------------------------|
| SVM                    | ~95–97%  | Best performance                       |
| Logistic Regression    | ~94–96%  | Strong and stable                      |
| Random Forest          | ~92–94%  | Good ensemble performance              |
| Naive Bayes            | ~90–93%  | Fast and efficient                     |
| Decision Tree          | ~85%     | Lower due to data complexity           |

---

## System Architecture

1. User inputs a message
2. Text preprocessing is applied
3. TF-IDF transforms the text
4. Each model predicts independently
5. Results are displayed (Spam / Ham)

---

## User Interface

A Streamlit-based interface was developed with:

- Text input box
- "Process" button
- Outputs from all 5 models
- Color-coded results:
  - Green: Ham
  - Red: Spam

---


