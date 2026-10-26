# Aspect-Based Sentiment Analysis on Financial News

## Overview
This project performs *Aspect-Based Sentiment Analysis (ABSA)* on financial news headlines. Unlike traditional sentiment analysis that assigns a single overall sentiment to an entire text, ABSA identifies specific entities (aspects) mentioned in the headline and predicts the sentiment toward each entity individually.

This is especially useful in finance, where a single news headline can contain multiple companies or topics with *conflicting sentiments*.

## Business Problem
Financial analysts and investors need fine-grained insights from news. A headline may be positive about one company and negative about another. Accurate entity-level sentiment helps with:
- Better investment decision-making
- Market sentiment monitoring
- Risk assessment and trading strategies

## Dataset
- *Name*: SEntFiN 1.0 (Aspect based Sentiment Analysis for Financial News)
- *Size*: 10,700+ human-annotated financial news headlines
- *Key Feature*: Over 2,800 headlines contain multiple entities, often with conflicting sentiments
- *Sentiment Labels*: Positive, Negative, Neutral
- *Paper*: Sinha et al. (2022) – SEntFiN 1.0: Entity-aware sentiment analysis for financial news

## Project Workflow

1. *Data Loading & Exploration*
   - Explored headline length, entity frequency, and sentiment distribution
   - Analyzed multi-entity headlines and conflicting sentiments

2. *Text Preprocessing*
   - Cleaning, tokenization, and preparation of text for modeling

3. *Feature Engineering *
   - Traditional approaches (TF-IDF) and modern embeddings

4. *Modeling*
   - Built classification models to predict sentiment for each entity
   - Explored classical ML & DL models and transformer-based approaches

5. *Evaluation*
   - Metrics: Accuracy, Precision, Recall, F1-Score 
   - Special attention to performance on multi-entity headlines

6. *Analysis & Insights*
   - Identified common patterns in positive/negative financial language
   - Examined model performance across different entity types

## Results
- *Best Model*: XGBoost
- *Performance*:
  - Accuracy: SVM: 0.36, XGBoost: 0.39
  - Macro F1-Score: SVM: 0.33, XGBoost: 0.36

## Key Insights
- Many financial headlines contain multiple entities with mixed sentiments — highlighting the importance of aspect-based approaches.
- Certain words and phrases strongly signal positive or negative sentiment toward specific companies or sectors.
- Handling multi-entity cases is more challenging than single-entity headlines.

## Technologies Used
- *Python*
- Pandas, NumPy
- NLTK / spaCy (text preprocessing)
- Scikit-learn (TF-IDF, classical models)
- Matplotlib, Seaborn, WordCloud (visualizations)

## Future Improvements
- Fine-tune transformer models (BERT, RoBERTa, FinBERT) for higher performance
- Deploy as a Streamlit app where users can paste a financial headline and get entity-level sentiments
- Expand to full news articles instead of only headlines
- Build a real-time financial news sentiment dashboard
