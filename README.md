# Arabic Fake News Detection using Evidence-Based Similarity

This project presents an Arabic NLP approach for fake news classification using semantic embeddings and evidence-based similarity features. The system combines tweet embeddings generated using AraBERT with cosine similarity scores computed against external fact-checking evidence.

The project was developed as part of a Master's level Machine Learning course.

---

## Project Overview

The goal of this project is to classify Arabic COVID-19-related tweets as real or fake using:

* Semantic tweet embeddings
* External fact-checking evidence
* Similarity-based feature engineering
* Traditional machine learning classifiers

The proposed approach compares tweet embeddings against verified fake and real evidence claims, generating two additional similarity features:

* Similarity to fake evidence
* Similarity to real evidence

These features are combined with text embeddings and evaluated using Logistic Regression and SVM classifiers.

---

## Methodology

### 1. Text Preprocessing

The tweets and evidence claims were cleaned using Arabic NLP preprocessing techniques, including:

* normalization
* punctuation removal
* stopword removal
* stemming/lemmatization

### 2. Embedding Generation

AraBERT sentence embeddings were generated for:

* tweets
* evidence claims

### 3. Evidence Similarity Features

Cosine similarity was computed between tweet embeddings and evidence embeddings to generate:

* `fake_sim`
* `real_sim`

### 4. Classification

The following classifiers were evaluated:

* Logistic Regression
* Support Vector Machine (SVM)

Performance was measured using:

* Accuracy
* F1-score
* Confusion Matrix

---

## Datasets

### ArCOV19-Rumors Dataset

Used for Arabic COVID-19 tweet classification.

Citation:

> Haouari, F., Hasanain, M., Suwaileh, R., Elsayed, T. (2021). ArCOV19-Rumors: Arabic COVID-19 Twitter Dataset for Misinformation Detection. Proceedings of WANLP 2021.

Dataset:
https://huggingface.co/datasets/asas-ai/ArCOV19-Rumors

---

### Arafacts Dataset

Used as the external evidence source for fact-checking claims.

Dataset:
https://huggingface.co/datasets/arbml/AraFacts

Only COVID-19-related claims were retained and used in this project.

---

## Results

The evidence-based approach showed a slight but consistent improvement over the baseline embedding-only model, demonstrating that external evidence similarity can provide additional useful signals for Arabic fake news detection.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Sentence Transformers
* AraBERT
* Matplotlib

---

## Disclaimer

This repository is intended for educational and research purposes only.

The datasets used in this project belong to their respective authors and providers.
