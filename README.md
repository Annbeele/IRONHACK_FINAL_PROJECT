![Good_news_robot](https://github.com/Annbeele/IRONHACK_FINAL_PROJECT/blob/main/FINAL%20PROJECT%20-%20Good%20News%20Robot/images/Robot-title-github.png)

<p align="center">
 <img src="https://img.shields.io/badge/python-v3.8%2B-blue">
 <img src="https://img.shields.io/badge/-Naive%20Bayes-yellowgreen">
 <img src="https://img.shields.io/badge/-NLP-red">
 <img src="https://img.shields.io/badge/-TF%20Vectorizer-ff69b4">
</p>

<p align = "center">
 <i> Anna Beteta, 2021 •
  Data Analytics Bootcamp - Ironack
 </i>
</p>



<h2 align="center"> 
  <a href="#project-description">PROJECT DESCRIPTION</a> •
  <a href="#approach">APPROACH</a> •
  <a href="#links">LINKS</a> 
</h2>

<br/><br/>

## PROJECT DESCRIPTION
Aren’t you tired of seeing so many bad news in the media?
Have you ever felt overwhelmed by all the concerning issues and catastrophic headlines we are bombarded with almost every day?

<p align = "center"> If your answer is yes, we got a plan for you! <p/>

**GoodNews**Robot consists of a real-time tool that gives you a quick insight about 🌈 good news 🌈 happening in the world. By gathering news articles from the last seven days, it displays a friendly visualization on the most frequent words from the main good-vibes topics.

It also predicts the category of each article and shows you a breakdown of good - neutral - bad news by category.

<p align="center">
<img src="https://github.com/Annbeele/IRONHACK_FINAL_PROJECT/blob/main/FINAL%20PROJECT%20-%20Good%20News%20Robot/images/WordCloud_today.png" alt="Wordcloud" width="350" height="250" class="center">

<img src="https://github.com/Annbeele/IRONHACK_FINAL_PROJECT/blob/main/FINAL%20PROJECT%20-%20Good%20News%20Robot/images/stacked_bar.png" alt="StackedBar" width="300" height="250" class="center">

 </p>
 
<br/><br/>

## APPROACH


### 1 - GATHERING BBC NEWS FROM API

We connect to [NewsApi](https://newsapi.org/) to gather news from the BBC (current to last 7 days). The information we choose to be provided by the API is:
- Title
- Description
- URL

This data is then cleaned and stored into a dataframe to prepare it for the next steps.
<br/><br/>

### 2 - CATEGORY PREDICTION
#### 2.1 - Training the model

<p>
 DATASET

In order to teach the model on how to classify news articles into categories, we use the <a href="https://www.kaggle.com/hgultekin/bbcnewsarchive">BBC News Archive Kaggle Dataset</a>. It consists of 2225 labelled articles from the BBC news website from 2004-2005, corresponding to five categories: business, entertainment, politics, sport and tech.
</p> 
 
<p> 
 MODEL: TF vectorizer + Naïve bayes

**GoodNews**Robot uses the Naïve Bayes approach to model news category predictors. It is a well-known algorithm which consists of a probabilistic classifier for binary and multi-class classification problems.

However, as the machine learning decision models can only process and learn from numerical feature vectors, we should encode the string data before applying Naïve Bayes. To do so, we use the TF (or term frequency) vectorizer, which quantifies a term's importance based on its frequency whithin a given document.


We then use the encoded data to feed into Naïve Bayes and train our model with the given dataset.
</p>

#### 2.2 - Predicting news categories
Once we cleaned the data form the API, we are ready to apply our trained model into new data and predict the category of each article.
<br/><br/>

### 4 - SENTIMENT ANALYSIS: Good - Neutral - Bad

**GoodNews**Robot uses the TextBlob library to perform a Sentiment Analysis. The sentiment property returns a namedtuple of the form Sentiment(polarity, subjectivity). The polarity score is a float within the range [-1.0, 1.0]. The subjectivity is a float within the range [0.0, 1.0] where 0.0 is very objective and 1.0 is very subjective.

In order to get more accurate results and overcome the inherent limitations of the API data (we don't have the whole content), **GoodNews**Robot only considers very polarized results when classifying news articles into good or bad news. That's why most of the news articles are considered neutral. The threshold used in our case is: >= 0.5 for the good and <= -0.5 for the bad.


## LINKS
- To run the script, you can download it by clicking on the following link:
[JUPYTER_NOTEBOOK](https://github.com/Annbeele/IRONHACK_FINAL_PROJECT/blob/main/FINAL%20PROJECT%20-%20Good%20News%20Robot/Good%20News%20Robot.ipynb)

- To see the presentation, click on the following link:
[Presentation](https://github.com/Annbeele/IRONHACK_FINAL_PROJECT/blob/main/FINAL%20PROJECT%20-%20Good%20News%20Robot/Good_News_Robot_Presentation.key)

- To see the Trello board, click on the following link:
[Trello](https://trello.com/b/wglu7YPy/good-news-robot)

<br/><br/>
