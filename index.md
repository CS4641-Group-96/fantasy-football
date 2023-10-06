---
layout: default
---

Our project about fantasy football.

# Intro / Background

# Problem / Definition

# Methods Algorithms and Libraries

## Methods

1. Data collection and processing
  * Deal with missing values
  * Possible label-encoding
1. Split data set into training and testing data (70/30 split)
1. Build ML models
1. Use metrics like Mean Absolute Error (MAE), Root Mean Squared Error to evaluate
1. Use model to predict player’s fantasy rating for 2023

The machine learning libraries that we plan to use are pandas, numpy, scikit-learn. Pandas is excellent for manipulating datasets. Numpy is excellent for mathematical operations, and Scikit-learn is excellent at scaling, creating regression models, and performance evaluation.

There are several types of regression models that we can use. We could implement a linear regression model to predict a player's fantasy point scores using his past fantasy point scores. We could also implement the SVR model by showing past player statistics and the fantasy points they scored for the model to learn the relationship between a player's performance and the points they score. (Once it has learned from the past, you can show it new data and ask the model to predict the fantasy points a player will score in 2023). Furthermore, we could implement a random forest model. The algorithm focuses on a random subset of players and a random subset of statistics. 

One tree might be an expert on quarterbacks using data from 2005-2015, while another might know about wide receivers from 2010-2022. Each tree looks at its subset of data and learns how player statistics relate to fantasy points. The model takes a majority vote to decide on the final prediction for testing data. Lastly, we could also use the KNN model to predict the value of a player's fantasy points based on the 'k' players with the most similar historical performance.

[Our Project's Dataset](https://fantasydata.com/nfl/fantasy-football-leaders?season=2022&seasontype=3&scope=1&subscope=1&startweek=1&endweek=1&aggregatescope=1&range=1).

# Results, Quantitative Metrics, and Discussion

# Peer-Reviewed References

* Beal, Ryan & Norman, Timothy & Ramchurn, Sarvapali. (2020). A Critical Comparison of Machine Learning Classifiers to Predict Match Outcomes in the NFL. International Journal of Computer Science in Sport. 19. 10.2478/ijcss-2020-0009. 

* J. R. Landers and B. Duperrouzel, "Machine Learning Approaches to Competing in Fantasy Leagues for the NFL," in IEEE Transactions on Games, vol. 11, no. 2, pp. 159-172, June 2019, doi: 10.1109/TG.2018.2841057.

* Wisdom, Conor and Javed, Aqib, Machine Learning for Data Analytics in Football: Quantifying Performance and Enhancing Strategic Decision-Making. Available at SSRN: https://ssrn.com/abstract=4558733 or http://dx.doi.org/10.2139/ssrn.4558733


# Project Timeline

Here is a link to our [Project Timeline](https://docs.google.com/spreadsheets/d/1PfeLZonz-8v8Uf2v6IxM1N3aaypRdWp5/edit?usp=sharing&ouid=115243335959569312831&rtpof=true&sd=true).

# Contribution Table

Below are the contributions of each of our members.

| Name                 | Contribution                                                                                      |
|:---------------------|:--------------------------------------------------------------------------------------------------|
| Emmanuel Ebhohimen   | Created GitHub Page, Contribution Table, Project Checkpoint, Project Timeline                     |
| Justin Huang         | Methods, Algorithms, and Libraries, Peer Reviewed References, Dataset, Project Checkpoint         |
| Gregory Elias        | Setup GitHub Repository and GitHub Pages, Video Presentation                                      |
| Joshua Abantao       | Intro / Background and Problem / Definition                                                       |
| Andrew Titus         | Results, Quantitative Metrics, and Discussion                                                     |

# Project Checkpoint

We plan to fully utilize the concepts we learned in class to this semester long project. From the class schedule, linear regression, logistic regression, and SVM will be covered in the future, so it excites us that we will be putting these machine learning models in practice. Random forest is another common machine learning algorithm/model that we plan to incorporate in our project because we believe that such an enhanced decision tree model is integral to formulating an accurate prediction model. After our proposal, we plan to start curating and manipulating our data site to fit our model. By the midterm report, we plan to already have a working data pipeline that filters data that fits our models, and would like to have already come up with the linear regression/logistic regression prediction model. After the mid term report, we plan to finalize on our random forest and our SVM model, and before the final report, complete the overall evaluation of our model, and successfully predict the fantasy scores for the NFL players next season.