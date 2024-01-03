# Sentiment Analysis of Tweets

This project focuses on sentiment analysis of tweets, employing various data processing and machine learning techniques. The core idea is to predict the sentiment of tweets as positive, negative, or neutral.



![Untitled](https://github.com/SimoneParvizi/Sentiment-Analysis/assets/75120707/b10f285c-b5a6-47e4-a55f-5f5c8d2b00bf)




# Getting Started
 
## Dataset

The dataset consists of tweets with labels indicating their sentiment. It is divided into training and test sets.

- `train.csv`: Contains tweets with their corresponding sentiment labels.
- `test.csv`: Contains tweets for which sentiment needs to be predicted.
- `sample_submission.csv`: A sample format for submission of predictions.

### Dataset Features

The dataset includes the following features:

- `text`: The text of the tweet.
- `sentiment`: The sentiment of the tweet (positive, negative, neutral).
- `selected_text`: A portion of the text that reflects the sentiment.

Additional features derived during analysis:

- Length of the tweet.
- Number of words in the tweet.
- Jaccard similarity score between `text` and `selected_text`.

## Features

The following features are extracted and used for training models:

- Length of tweets.
- Number of words in tweets.
- Preprocessing steps like lowercasing, lemmatization, and removal of stopwords.
- TF-IDF vectorization of the cleaned text.
- Meta features like word count differences and Jaccard similarity scores.

## Model Training

Two machine learning models are used:

1. **Logistic Regression**
2. **Random Forest Classifier**

These models are trained on the TF-IDF vectors of the preprocessed tweet texts.

## Evaluation

The models are evaluated using accuracy and F1-score. Additionally, a confusion matrix is displayed for a visual representation of the model's performance.

## How to Run

- Load and preprocess the data.
- Extract features and split the data into training and test sets.
- Train the models on the training set.
- Evaluate the models on the test set.
- Use the best-performing model to make predictions on new data.

## Example Prediction

```python
new_tweet = "Although I don't like Harry Potter, I still watched it and it was pretty good"
predicted_sentiment = predict_sentiment(new_tweet)
print("Predicted Sentiment:", predicted_sentiment)
