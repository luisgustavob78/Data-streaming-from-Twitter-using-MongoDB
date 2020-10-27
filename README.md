# Data-streaming-from-Twitter-using-MongoDB

## Introduction
A huge part of social network data is generated on Twitter. This media channel is a place where people express their opinions, ideologies and ideas. Looking at that, this social network can be an importa source of data to evaluate the society's behavior in face of public policies. In this project, we use tweets to analyze with machine learning the public opinion in Brazil about the new vaccine against coronavirus.

## Connection with Twitter

The first step is to set the connection between the enviroment and twitter, as following

![](https://github.com/luisgustavob78/Data-streaming-from-Twitter-using-MongoDB/blob/main/twitter_connection.png)

## Connection with MongoDB

After the connection with Twitter, we need a database to storage our tweets. Here he have unstructered data, so we need a noSQL database. In this project, i used MongoDB. We can do that using the MongoDB software avaliable on the cloud;

![](https://github.com/luisgustavob78/Data-streaming-from-Twitter-using-MongoDB/blob/main/mongodb_connection.png)

## Data Preprocessing

With our two connections ready, we can collect our data in real-time. The scraping was ran for 30 minutes and got 1647 tweets. With this data, our first treatment was a preprocessing to get it cleaner and ready for a good analysis. The steps ran were:

* Converting the words to lower;
* Removing stopwords for portuguese language;
* Removing accents;
* Getting the steam of the words to reduce the amount of data.

![](https://github.com/luisgustavob78/Data-streaming-from-Twitter-using-MongoDB/blob/main/preprocessing_data.gif)

## Data Analysis

Now that we have a clean data, we can run some analysis. To understand what people are talking about the coronavirus vaccine, we can look at the most used words and phrases:

![](https://github.com/luisgustavob78/Data-streaming-from-Twitter-using-MongoDB/blob/main/data_analysis.gif)

An intersting point is that people are talking a lot something like "nao vou tomar vacina". It means that a significant number of people is considering to not take the vaccine. The main causes for this is that the vaccine is a test yet and many people are afraid about the side effects.

## Machine Learning Model

To evaluate the sentiment of people on those tweets, i used a multibinomial Naive-Bayes model with a labeled data 'Tweets_Mg.csv'. With this asset i got a model with 94% of accuracy.

![](https://github.com/luisgustavob78/Data-streaming-from-Twitter-using-MongoDB/blob/main/training_results.gif)

With a trained model, i made some predictions. The most tweets is neutral, but there are most positive comments about the vaccine in Brazil than negative.

![](https://github.com/luisgustavob78/Data-streaming-from-Twitter-using-MongoDB/blob/main/results.png)

## Installation

All this code was ran at colab. The only installations needed there was:

```
pip install unidecode
```

```
nltk.download('stopwords')
```
