# News Classifier 

***News Classifier*** is a machine learning project whose goal is to classify newspaper articles into five different categories. 

The project is inspired by a series of three articles by Miguel Fernández Zafra.

https://towardsdatascience.com/text-classification-in-python-dd95d264c802

The data was aquired at different newspapers than those in that project. 

The project is split into three main parts. 

## Web Scraping

We use BeautifulSoup to extract news articles from *La Presse* and *Le Journal de Montreal*. We extracted the articles from the archives and from the most recent news of the day. 

The datas are contained in the folder ***Data*** and the web scraping is performed in the files in the ***Web Scraping*** folder. 

## Data Cleaning and Data Analysis

We clean, analyze and prepare the datas for features engineering using text representation methods. We use 'TF-IDF' Vectors as our feature engineering.

This is done in the folder ***Data Cleaning***. 

## Machine Learning Model

We test several models: 

- Support Vector Machine 
- Random Forest
- K Nearest Neighbors 
- Ridge Regression

This is done in the folder ***Model Training***. K Nearest Neighbors and Support Vecor Machine were tested using explicitely cross validation and (Random) Grid Search. Ridge Regression, Random Forest and Support Vecor Machine were tested and compared using AutoML with Neuraxle (https://www.neuraxle.org). 

## Coming Next

Next we will deploy the model using flask. 