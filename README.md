# GOOD NEWS ROBOT
## IRONHACK FINAL PROJECT
by [Anna Beteta](https://github.com/Annbeele), July 2021
<br/><br/>

![Good_news_robot](https://github.com/Annbeele/IRONHACK_FINAL_PROJECT/blob/main/FINAL%20PROJECT%20-%20Good%20News%20Robot/Good_News_Robot_wallpaper.png)


## SCENARIO
Aren’t you tired of seeing so many bad news in the media?
GOOD NEWS Robot is here to help!  

**MAIN TOOLS: Naive-Bayes, TF Vectorizer, NLP, Sentiment Analysis**

<br/><br/>
 
### WHAT DOES THE GOOD NEWS ROBOT DO?
It gathers news articles from the last 7 days until today
It classifies the news into categories
To keep you informed about latest GOOD NEWS in the world
<br/><br/>

### WORKFLOW

1. TRAINING THE MACHINE LEARNING MODEL
- We used TF vectorizer + Naive-Bayes to train the robot on how to predict news articles categories.
- As Naive-Bayes is a supervised model, we trained it with a labelled dataset:
[BBC_archive_dataset](https://github.com/Annbeele/IRONHACK_FINAL_PROJECT/blob/main/FINAL%20PROJECT%20-%20Good%20News%20Robot/bbc-news-data.csv)

2. GET NEWS FROM API: Using NewsAPI Source = BBC News
- We get the title, description and URL

3. PREDICTING NEWS CATEGORIES


5. PERFORM SENTIMENT ANALYSIS WITH TEXTBLOB


7. GET VISUALIZATIONS
- Stacked bar chart --> to get insights about most published categories, broken down by good/bad/neutral news
- WordCloud just for GOOD NEWS --> most frequent words in GOOD NEWS
<br/><br/>
- Here we can see a WordCloud example (remember it updates everytime you run the code!):
![WordCloud_example](https://github.com/Annbeele/IRONHACK_FINAL_PROJECT/blob/main/FINAL%20PROJECT%20-%20Good%20News%20Robot/WordCloud_today.png)


## LINKS
- To see the script, click on the following link:
[JUPYTER_NOTEBOOK](https://github.com/Annbeele/IRONHACK_FINAL_PROJECT/blob/main/FINAL%20PROJECT%20-%20Good%20News%20Robot/Good%20News%20Robot.ipynb)

- To see the presentation, click on the following link:
[Presentation](https://github.com/Annbeele/IRONHACK_FINAL_PROJECT/blob/main/FINAL%20PROJECT%20-%20Good%20News%20Robot/Good_News_Robot_Presentation.key)

- To see the Trello board, click on the following link:
[Trello](https://trello.com/b/wglu7YPy/good-news-robot)

<br/><br/>
