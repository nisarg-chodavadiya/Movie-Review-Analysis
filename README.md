# Movie-Review-Analysis
This analysis is the answer to one question which is 
‘Which thing in movie people’s attention drawn most towards it in any movie?’
Easiest Model built with high accuracy for sentiment analysis for reviews by logistic regression.

# Dataset
Stanford IMDB Dataset was used in this project which was originally published by researchers of Stanford University. 
Link: http://ai.stanford.edu/~amaas/data/sentiment/

# Preprocessing
## Part 1: Kaggle dataset with rating and sentiment columns 
It is a major part of which the whole dataset converted in CSV formate with columns Review, Rating, Sentiment by file handling and this preprocessed dataset I am putting on Kaggle and in this project I am using that dataset.
Link:
https://www.kaggle.com/nisargchodavadiya/imdb-movie-reviews-with-ratings-50k
## Part 2: Preprocess the text to analyze (Text Clean)
For sentiment analysis text in the whole dataset cleaned by removing punctuation and stop words.
## Part 3: Process text for algorithm for sentiment analysis
Applied STEM on the cleaned text and then converted TF-IDF vectors.

# Model
A very simple Logistic Regression algorithm applied to get higher accuracy more than given in TensorFlow website with RNN with LSTM https://www.tensorflow.org/tutorials/text/text_classification_rnn#stack_two_or_more_lstm_layers

Accuracy of Logistic Regression model without tuning 88% on test data. 
![CM for IMDB Case Study](https://user-images.githubusercontent.com/75474944/117927560-fe7a9c00-b317-11eb-99bb-a8b0ece54aa7.png)
