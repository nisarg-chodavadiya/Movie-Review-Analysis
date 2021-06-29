# Movie Review Analytics
1. Problem Statement: 
**What people will look at in the movie at a first glance, regardless of genre?** as **More Insights on Reviews.** **"Movie production house wants to know, What people will look at in the movie at first glance, regardless of genre?"**
2. Publish a unique dataset on kaggle in CSV format with rating and sentiment both columns for each review from Stanford IMDB dataset. (Preprocessing with File handling in python for 100K txt files to two CSV with 50K labeled and 50K unlabeled)
3. Easiest model build with high accuracy for sentiment analysis for reviews by logistic regression.
4. Sentiment Score Analysis in Transformer as predicting ratings.

# Dataset
Stanford IMDB Dataset was used in this project which was originally published by researchers of Stanford University. 
In this dataset there are thousands of movie reviews collected as in 30 reviews per movie, 50-50% positive-negative to get insight.
Original Link: http://ai.stanford.edu/~amaas/data/sentiment/

# Preprocessing
## Part 1: Kaggle dataset with rating and sentiment columns 
It is a major part of which the whole dataset is converted in CSV format with columns Review, Rating, Sentiment by file handling in python and this preprocessed dataset I am putting on Kaggle and in this project I am using that dataset.</br>
Link: https://www.kaggle.com/nisargchodavadiya/imdb-movie-reviews-with-ratings-50k </br>
Which is looking like this:</br>
![Data Frame Snap Shot](https://user-images.githubusercontent.com/75474944/117930709-f45a9c80-b31b-11eb-8aa1-bafeb59a6d97.PNG)

## Part 2: Preprocess the text to analyze (Text Clean)
For sentiment analysis text in the whole dataset cleaned by removing punctuation and stop words.
## Part 3: Process text for algorithm for sentiment analysis
Applied STEM on the cleaned text and then converted TF-IDF vectors.

# Model
A very simple Logistic Regression algorithm applied to get higher accuracy more than given in TensorFlow website with RNN, LSTM network https://www.tensorflow.org/tutorials/text/text_classification_rnn#stack_two_or_more_lstm_layers

Accuracy of Logistic Regression model without tuning 88% on test data. 
![CM for IMDB Case Study](https://user-images.githubusercontent.com/75474944/117927560-fe7a9c00-b317-11eb-99bb-a8b0ece54aa7.png)

## Sentiment Score Analysis in Transformer (Predicting Rating of Review)
In this analysis random, 1000 reviews were taken and predicted sentiment score through pre-trained model form "nlptown/bert-base-multilingual-uncased-sentiment" and compared to rating column. In the rating column, I already converted ratings 0-5 scale from 0-10 for these 1000 reviews.
![image](https://user-images.githubusercontent.com/75474944/123746650-8a985100-d8cf-11eb-8e3f-cb1eebdaac6c.png)

# More Insights on Reviews
Word Cloud on positive and negative reviews can answer superficially to the question that is “Which thing in a movie people’s attention is drawn most towards it in any movie?”

## Preprocessing for Word Cloud
That is the most sensitive step which only can give superficial insight on this question.
Remove stopwords and punctuations, HTML tags, and combine all positive reviews. Then followed the same for negative reviews.
Feed this to word cloud and the next preprocess to insight can only be done directly at word cloud.
 
## Word Cloud
In this word cloud, notice the biggest word if it is a common word which is not leading to insight to question then add that word in stop words for word cloud and plot word cloud again up to when the first word which can derive insight from the word cloud.

Positive Reviews Word Cloud:
![Positive reviews](https://user-images.githubusercontent.com/75474944/117929690-b90b9e00-b31a-11eb-9cd5-b262cdd442ee.png)

Negative Reviews Word Cloud:
![Negative reviews](https://user-images.githubusercontent.com/75474944/117929702-bc068e80-b31a-11eb-84df-42cb8c7782d7.png)

# Conclusion
Answer to Question:
1. People looks at the character, story in the movie at first glance.
2. Then they looked at the scene.
3. Many times the story, scene makes the movie bad when the movie gets low ratings.</br>
Note: This dataset was published in 2011 so today’s reviews may make a difference in the answer to this question.
