# News Classifier 

***News Classifier*** is a machine learning project whose goal is to classify newspaper articles into four different categories. 

The project is inspired by a series of three articles by Miguel Fernández Zafra.

https://towardsdatascience.com/text-classification-in-python-dd95d264c802

The data was aquired at different newspapers than those in that project. 

The project is split into three main parts. 

## Web Scraping

We use BeautifulSoup to extract news articles from *La Presse* and *Le Journal de Montreal*. We extracted the articles from the archives and from the most recent news of the day. 

The datas are contained in the folder ***Data*** and the web scraping is performed in the files in the ***Web Scraping*** folder. 

## Data Cleaning and Data Analysis

We clean, analyze and prepare the datas for features engineering using text representation methods. We use 'TF-IDF' Vectors as our feature engineering.

An analysis allowed us to see that one of the categories, 'actualites', was too vague and would create some misclassification. We therefore decided to remove it from our modelisation. 

This is done in the folder ***Data Cleaning***. 

## Visualisation 

Using t-SNE to reducte dimension, we obtain the following plot.

![tsne_svc](/Data cleaning/tsne_svc.png)

## Machine Learning Models

We test several models: 

- Support Vector Machine 
- Random Forest
- K Nearest Neighbors 
- Ridge Regression

This is done in the folder ***Model Training***. K Nearest Neighbors and Support Vecor Machine were tested using explicitely cross validation and (Random) Grid Search. Ridge Regression, Random Forest and Support Vecor Machine were tested and compared using AutoML with Neuraxle (https://www.neuraxle.org). 

Support Vector Machine performed best with a 91% accuracy. It obtained a 99% accuracy score on training data, a typical sign of overfitting. However, we decided to train only on older articles and test on the newest articles, so the discrepancy could be explained by that. The reason for doing it this way is that we wanted to make sure that our model would work on new articles after deploying it. 

## Coming Next

Next we will deploy the model using flask. 