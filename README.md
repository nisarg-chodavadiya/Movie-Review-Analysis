# Movie-Review-Analysis
1. This analysis is the answer to one question which is 
"Which thing in movie people’s attention drawn most towards it in any movie?" as “More Insights on Reviews”.
2. Easiest Model built with high accuracy for sentiment analysis for reviews by logistic regression.

# Dataset
Stanford IMDB Dataset was used in this project which was originally published by researchers of Stanford University. 
In this dataset there are thousands of movie reviews were collected as in 30 reviews per movie, 50-50% positive-negative to get insight.
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

# More Insights on Reviews
Word Cloud on positive and negative reviews can answer a superficially to question that is “Which thing in movie people’s attention drawn most towards it in any movie?”

## Preprocessing for Word Cloud
That is the most sensitive step which only can give superficial insight on this question.
Remove stopwords and punctuations, HTML tags, and combine all positive reviews. Then followed same for negative reviews.
Feed this to word cloud and the next preprocess to insight can only be done directly at word cloud.
 
# Word Cloud
In this word cloud, notice the biggest word if it is a common word which is not leading to insight to question then add that word in stop words for word cloud and plot word cloud again up to when the first word which can derive insight from the word cloud.

Positive Reviews Word Cloud:
![Positive reviews](https://user-images.githubusercontent.com/75474944/117929690-b90b9e00-b31a-11eb-9cd5-b262cdd442ee.png)

Negative Reviews Word Cloud:
![Negative reviews](https://user-images.githubusercontent.com/75474944/117929702-bc068e80-b31a-11eb-84df-42cb8c7782d7.png)

# Conclusion
For the answer and final words on world cloud please refer to the conclusion section of the notebook.
