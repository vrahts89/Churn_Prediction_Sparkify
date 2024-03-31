# Churn Prediction Sparkify

## Project Sparkify
A Pyspark capstone project within the Udacity Data Science program. Its primary objective is to forecast churn for Sparkify, an imaginary music streaming platform designed to mirror real-world services like Spotify.

## File Descriptions

- Sparkify.ipynb - Jupyter Notebook with all the project code.
- README.md

## Motivation
For me the motivation for this project lied in the application of the PySpark language since I am working with decentralized data and computing on a daily basis and this project improved my Pyspark knowledge by a lot. The project provided access to both a small sample dataset, which was accessible locally, and a large 12GB dataset hosted on an Amazon EMR cluster. I only worked on the small dataset, since I am still lacking sufficient AWS knowledge. However, this will be my next task to tackle.

## Project Overview
In business terms, "churn" refers to customers who discontinue using a company's service within a specified timeframe. Businesses aim to preemptively identify users who may leave in order to take proactive measures to retain them.

Sparkify users have the option to stream music via a free subscription plan with ads or a paid plan without ads. In addition to listening to music, users can interact with the service by giving thumbs up or down, adding songs to playlists, or connecting with friends. Users have the flexibility to switch subscription plans by upgrading from free to paid, downgrading from paid to free, or canceling the subscription altogether. Churned users in our project are defined as those who downgrade or cancel their subscription. We focus separately on these two churn types: canceled and downgraded users.

The project's objective is to develop a machine learning model capable of accurately identifying churned users of each type based on selected metrics and anticipated outcomes.

## Project Approach

### Data Cleaning:
Identified and removed empty userIds, eliminating 8346 rows. Corrected missing gender values by removing corresponding empty user IDs.

### Data Analysis:
Visual data analysis regarding churn rates for the indivual values per feature.

### Feature Engineering:
Created a dataframe with categorical (gender, operating system, subscription level) and numerical features (number of songs per session, number of add to playlist actions, number of thumbs down actions, number of thumbs up actions, number of friends added actions, number of distinct artists listened to, number of days since registering)

### Machine Learning Modeling:
Trained and compared 4 different models:

+ Logistic Regression
+ Gradient Boosting
+ Naive Bayes
+ Random Forest
  
### Parameter Tweaking:
Fine-tuned Random Forest parameters using cross-validation.

### Results:
Random Forest achieved the highest f1-score (0.62) and accuracy (0.68) with optimal parameters after cross validation. Identified key feature importance.

### Shortcomings:
The feature engineering needs to be improved since the problem of overfitting occurred.

### Blogpost
Additionally I wrote a Blogpost on medium describing the thought process and the results in detail. You can find it with this link: 
https://medium.com/@vrahts_22290/predicting-churn-in-a-streaming-subscription-model-31a8e1e7c410

## Libraries Used

-pyspark (SparkConf, SparkSession, functions, ml)
-pandas
-numpy
-matplotlib.pyplot
-seaborn

## Acknowledgements
Thanks to Udacity for the unique "big data experience" with spark.
