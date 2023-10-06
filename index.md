---
layout: default
---

* * *

# Intro / Background

Fantasy football allows fans to manage their own team of players. To compete, fantasy teams earn points based on the performances of their players during real NFL games. However, It is common for players to exceed or underperform compared to their expectations. With a multitude of factors such as injuries, matchup grades, and team strategies, how can one accurately predict player performances? This project aims to address that using the default PPR scoring system.

# Problem / Definition

We aim to predict the rankings for how players will perform during the football season using machine learning.

# Methods Algorithms and Libraries

## Methods

1. Data collection and processing
  - 1a) Handle missing values
  - 1b) Possible label-encoding
3. Split data set into training and testing data (70/30 split)
4. Build ML models
5. Use metrics like Mean Absolute Error (MAE), Root Mean Squared Error to evaluate
6. Use metrics: Mean Absolute Error (MAE), Root Mean Squared Error (RMSE) to evaluate
7. Use model to predict player’s fantasy rating for 2023

Our machine learning libraries of interest are pandas (for manipulating datasets), numpy (for mathematical operations), and scikit-learn (for scaling, creating regression models, and performance evaluation). 

There are several types of regression models that we can use. We could implement a linear regression model to predict a player's fantasy point scores using past fantasy scores. We could also implement the SVR model to learn the relationship between a player's performance and the points they score using past player statistics and fantasy points. (Once it has learned from the past, it can predict a player’s 2023 fantasy points with new data). Furthermore, we could implement a random forest model. The algorithm focuses on a random subset of players and a random subset of statistics. One tree might be an expert on quarterbacks using data from 2005-2015, while another might know about wide receivers from 2010-2022. Each tree looks at its subset of data and learns how player statistics relate to fantasy points. The model takes a majority vote to decide on the final prediction for testing data. Lastly, we could also use the KNN model to predict the value of a player's fantasy points based on the 'k' players with the most similar historical performance. 
 

[Our Project's Dataset](https://fantasydata.com/nfl/fantasy-football-leaders?season=2022&seasontype=3&scope=1&subscope=1&startweek=1&endweek=1&aggregatescope=1&range=1).

# Results, Quantitative Metrics, and Discussion

Our project's goal is to compare our model with the actual scoring output of the 2023 season. By the end of our timeline, 11-12 weeks of the 17-18 week fantasy football season will be complete. We can adjust the actual scoring output from the first 11-12 weeks of the season to provide an estimated output after 18 weeks to compare with our model. We will use MAE or RMSE to compare the results of the model with the actual results of players this season.

Additionally, we can create a tiered ranking for each position and compare this with both the actual rankings of 2023 and the preseason rankings by experts  (e.g. [PFF](https://www.pff.com/news/fantasy-football-rankings-2023-top-250)). If our model shows better results than preseason draft rankings, our model could help users determine players who may not be valued by traditional experts.

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
| Emmanuel Ebhohimen   | Created GitHub Page, Contribution Table, Project Timeline                                         |
| Justin Huang         | Methods, Algorithms, and Libraries, Peer Reviewed References, Dataset, Project Checkpoint         |
| Gregory Elias        | Setup GitHub Repository and GitHub Pages, Video Presentation                                      |
| Joshua Abantao       | Intro / Background and Problem / Definition                                                       |
| Andrew Titus         | Results, Quantitative Metrics, and Discussion                                                     |

# Project Checkpoint

We plan to fully utilize the concepts we learned in class to this semester long project. From the class schedule, linear regression, logistic regression, and SVM will be covered in the future, so it excites us that we will be putting these machine learning models in practice. Random forest is another common machine learning algorithm/model that we plan to incorporate in our project because we believe that such an enhanced decision tree model is integral to formulating an accurate prediction model. After our proposal, we plan to start curating and manipulating our data site to fit our model. By the midterm report, we plan to already have a working data pipeline that filters data that fits our models, and would like to have already come up with the linear regression/logistic regression prediction model. After the mid term report, we plan to finalize on our random forest and our SVM model, and before the final report, complete the overall evaluation of our model, and successfully predict the fantasy scores for the NFL players next season.
