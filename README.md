# Sentiment Analysis of Amazon Product Reviews

## Project Overview

This project involves building a sentiment analysis model using Amazon product reviews. The main objective is to classify product reviews as either **positive** or **negative** based on the `overall` rating provided by the reviewer.

### Key Steps:
1. **Data Preprocessing**: 
   - Cleaned the review text by removing punctuation, numbers, and stopwords.
   - Converted the text to lowercase.
   
2. **Feature Extraction**: 
   - Used TF-IDF (Term Frequency-Inverse Document Frequency) to transform the cleaned text into numerical features.
   
3. **Sentiment Labeling**: 
   - Mapped review ratings (1-5) into sentiment labels:
     - Ratings 4-5: Positive (labeled as `1`)
     - Ratings 1-2: Negative (labeled as `0`)
     - Ratings of 3 were excluded (neutral).
     
4. **Model Training**: 
   - Trained a Logistic Regression model on the training dataset.
   - Evaluated the model on the test dataset, achieving an accuracy of **92%**.

## Dataset

The dataset used for this project contains Amazon product reviews. It includes the following columns:
- `reviewText`: The textual content of the review.
- `overall`: The rating of the product (1-5).
- `sentiment`: The sentiment label derived from the rating.

## Model Performance

The model achieved an accuracy of **92%** on the test dataset, with particularly high performance on positive reviews.

| Metric       | Precision | Recall | F1-score |
|--------------|-----------|--------|----------|
| **Positive** | 0.94      | 0.98   | 0.96     |
| **Negative** | 0.83      | 0.59   | 0.69     |

## Requirements

To run this project, you'll need:
- Python 3.x
- Libraries: `pandas`, `scikit-learn`, `nltk`

Install the necessary libraries using:
```bash
pip install -r requirements.txt
