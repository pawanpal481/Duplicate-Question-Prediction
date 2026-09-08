# Duplicate Question Prediction

A Machine Learning project that predicts whether two given questions are **duplicate questions or not**.

The project uses Natural Language Processing (NLP) techniques and a **Random Forest Classifier** to compare two questions based on various text similarity and linguistic features.

## 🚀 Live Demo

The application is deployed using Streamlit Community Cloud.

**Live App:**  
https://duplicate-question-prediction.streamlit.app/

## 📌 Project Overview

Duplicate questions are questions that have different wording but have the same or very similar meaning.

For example:

**Question 1:**
> What is machine learning?

**Question 2:**
> What do you mean by machine learning?

These questions have the same meaning and should be classified as duplicate questions.

The application takes two questions as input and predicts:

- `1` → Duplicate
- `0` → Not Duplicate

## 🧠 Machine Learning Approach

The project uses **Natural Language Processing (NLP)** and feature engineering to convert text into numerical features.

The following features are extracted from the question pairs:

### 1. Basic Features

- Length of Question 1
- Length of Question 2
- Number of words in Question 1
- Number of words in Question 2
- Number of common words
- Total number of words
- Common word ratio

### 2. Token Features

Token-based features include:

- Common non-stopwords
- Common stopwords
- Common tokens
- Minimum and maximum token overlap
- First word similarity
- Last word similarity

### 3. Length Features

The model uses:

- Absolute difference in question length
- Average token length
- Longest common substring similarity

### 4. Fuzzy Matching Features

The following fuzzy matching techniques are used:

- QRatio
- Partial Ratio
- Token Sort Ratio
- Token Set Ratio

### 5. Bag of Words

A CountVectorizer is used to convert the processed questions into numerical vectors.

The final feature vector contains **6022 features**.

## 🤖 Model

The project uses:

**Random Forest Classifier**

The trained model is saved as:

```text
model.pkl
