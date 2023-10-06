---
layout: default
---

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

One tree might be an expert on quarterbacks using data from 2005-2015, while another might know about wide receivers from 2010-2022. Each tree looks at its subset of data and learns how player statistics relate to fantasy points. The model takes a majority vote to decide on the final prediction for testing data. Lastly, we could also use the KNN model to predict the value of a player's fantasy points based on the 'k' players with the most similar historical performance. We won't be using logistic regression because classification algorithms do not provide exact point projections.

[Our Project's Dataset](https://fantasydata.com/nfl/fantasy-football-leaders?season=2022&seasontype=3&scope=1&subscope=1&startweek=1&endweek=1&aggregatescope=1&range=1).

# Results, Quantitative Metrics, and Discussion

# Peer-Reviewed References

# Project Timeline

# Contribution Table

Below are the contributions of each of our members.

| Name                 | Contribution                                                                  |
|:---------------------|:------------------------------------------------------------------------------|
| Emmanuel Ebhohimen   | Created GitHub Page, Contribution Table, Project Checkpoint, Project Timeline |
| Justin Huang         | Methods, Algorithms, and Libraries, Peer Reviewed References, Dataset         |
| Gregory Elias        | Setup GitHub Repository and GitHub Pages, Video Presentation                  |
| Joshua Abantao       | Intro / Background and Problem / Definition                                   |
| Andrew Titus         | Results, Quantitative Metrics, and Discussion                                 |

# Project Checkpoint

### Small image

![Octocat](https://github.githubassets.com/images/icons/emoji/octocat.png)

### Large image

![Branching](https://guides.github.com/activities/hello-world/branching.png)