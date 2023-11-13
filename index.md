---
layout: default
---

* * *

# Intro / Background

Fantasy football allows fans to manage their own team of players. To compete, fantasy teams earn points based on the performances of their players during real NFL games. However, it is common for players to exceed or underperform compared to expectations. With a multitude of factors such as injuries, matchup grades, and team strategies, how can one accurately predict player performances? This project aims to address that using the default PPR scoring system. A large dataset featuring football player data from 2019 - 2022 will be used to create the model and player data from 2023 (also included in the dataset) will be used to test the model's accuracy. This dataset is especially valuable as it contains features such as players' snaps per game, their expected fantasy points for the season, and red zone snaps per game, which will allow for more accurate modelling. A notable project that has been done in fantasy football is an artificial intelligence that gives real-time recommendations on players in fantasy teams. With this project, we hope to do the same, except instead of real-time updates, we predict the fantasy points for all NFL quarterbacks for the upcoming season (before it has even started!) so fantasy teams can choose the best players and win their league.

[Our Project's Dataset](https://www.4for4.com/nfl-player-stat-explorer).


# Peer-Reviewed References

* R, P. (n.d.). Ai-powered fantasy sports for accurate data analytics. AI-powered Fantasy Sports for Accurate Data Analytics. https://www.intuz.com/blog/ai-powered-fantasy-sports
  
* Beal, Ryan & Norman, Timothy & Ramchurn, Sarvapali. (2020). A Critical Comparison of Machine Learning Classifiers to Predict Match Outcomes in the NFL. International Journal of Computer Science in Sport. 19. 10.2478/ijcss-2020-0009. 

* J. R. Landers and B. Duperrouzel, "Machine Learning Approaches to Competing in Fantasy Leagues for the NFL," in IEEE Transactions on Games, vol. 11, no. 2, pp. 159-172, June 2019, doi: 10.1109/TG.2018.2841057.

* Wisdom, Conor and Javed, Aqib, Machine Learning for Data Analytics in Football: Quantifying Performance and Enhancing Strategic Decision-Making. Available at SSRN: https://ssrn.com/abstract=4558733 or http://dx.doi.org/10.2139/ssrn.4558733


# Problem / Definition

To help fans get the best chance at having a high-powered team, we aim to help them identify the best players. More specifically, what better way to do such than to predict the highest-scoring fantasy position, the quarterback? We aim to predict the rankings/fantasy points for all NFL quarterbacks using machine learning for the upcoming season so that fantasy teams can pick the best players and win their league.

# Methods Algorithms and Libraries

## Methods

1. Data collection and processing

We downloaded quarterback fantasy statistics from 2019, 2020, 2021, 2022, and 2022 in the form of csv from "https://www.4for4.com/nfl-player-stat-explorer". Here is a snippet of the format and data of each csv file:

![csv ss](/fantasy-football/assets/css/1.png)


After downloading the data in the form of multiple csv files, we loaded the data into our machine learning environment and into separate Pandas dataframes. These 5 separate data frames are then concatenated into a single data frame for processing:

![csv ss](/fantasy-football/assets/css/2.png)

Here is a snippet of the semi-processed data and its column names:

![csv ss](/fantasy-football/assets/css/3.png)

![csv ss](/fantasy-football/assets/css/3.5.png)


Then, we transformed categorical features using OneHotEncoder, converting categorical variables into a more efficient format that could be provided to ML algorithms to do a better job in prediction. We also used ColumnTransformation to preprocess different subsets of features, and that left numeric features "untransformed" and ensured only the relevent features are included in the model training process. In addition, we used scaling and normalization for our SVR algorithm to improve SVR performance:

![csv ss](/fantasy-football/assets/css/4.png)

![csv ss](/fantasy-football/assets/css/4.5.png)


3. Split data set into training and testing data (80/20 split)

We have the dataset for 2019, 2020, 2021, 2022, and 2023, so we decided th use 2019, 2020, 2021, 2022 as training data, and use 2023 as our testing data, hence a 80/20 split. The intention is to use data from previous years to train the model and test it on the most recent year's data

![csv ss](/fantasy-football/assets/css/5.png)


5. Build ML models

We initialized and trained various regression models on the training set. The machine learning models used in this porject include linear regression, ridge regression, lasso regression, random forest, gradient boosting, and SVR: 

![csv ss](/fantasy-football/assets/css/6.png)


Results

As a recap, we used 2019, 2020, 2021, 2022's fantasy data to train a machine learning model, and after constructing the models, we used 2023's fantasy data to test the accuracy of the model. Here is the data predicted by various different machine learning models. For clarity purposes, we placed the predicted data next to 2023's actual data. 

![csv ss](/fantasy-football/assets/css/7.png)

![csv ss](/fantasy-football/assets/css/7.5.png)

![csv ss](/fantasy-football/assets/css/7.8.png)

![csv ss](/fantasy-football/assets/css/7.9.png)

![csv ss](/fantasy-football/assets/css/7.66.png)

![csv ss](/fantasy-football/assets/css/7.22.png)


Analysis and Discussion

Here are the graphs that show the relationship between predicted data and actual data using Matplotlib:

![csv ss](/fantasy-football/assets/css/8.png)


As shown, the model relatively accurately predicted the fantasy points for 2023. To further show the relationship between predicted and actual data, we calculated the mean squared error (MSE) for each model:

![csv ss](/fantasy-football/assets/css/9.png)


Which model performs the best? Here is a chart that visualizes the MSE for each model:

![csv ss](/fantasy-football/assets/css/10.png)


As shown, linear regression has the best performance, followed by ridge regression and gradient boosting. 


These results show promise as fantasy football players often do better as they are more skilled, which is reflected in the visuals we've generated. As this skill allows players to accumulate impactful fantasy stats such as yardage and touchdowns, it makes sense that these players would perform better than their counterparts. This makes for a generally linear relationship, giving reason as to why our linear regression model had the smallest mean squared error value out of our 6 models. However, it is important to consider the possibility of overfitting as our linear regression model had a notably smaller mean squared error around 10^-25 compared to a value around 10^-5 for the other models. Our data colection included a variety of features introduced some complexity to the learning process. Our other models such as ridge regression and gradeitn boosting were better equipped to handle this. Ridge regression being the next best model could be attributed to this model's ability to utilize coefficient shrinkage to create reflective predictions while discouraging overfitting. On the other hand, gradient boosting's ability to handle complex realtionships, correct boosting errors, and handle classifications likley was able to adjust well compared to the other models. Even as these two models were the next best (after linear regression), it's important to note the closeness of mean squared error values among all models apart from linear regression. These had a mean squared error at most 10^-5 away from each other which suggest comparability of results to an extent. Perhaps accurate models for this proejct must be able to handle larger complexities well. Perhaps it's simply that fantasy football is more easily predictable for quarterbacks, resulting in a more easily discernable data pattern that anticipated. We plan to refine these results in further iterations of our testing and implementations.



# Project Timeline

Here is a link to our [Project Timeline](https://docs.google.com/spreadsheets/d/1PfeLZonz-8v8Uf2v6IxM1N3aaypRdWp5/edit?usp=sharing&ouid=115243335959569312831&rtpof=true&sd=true).

# Contribution Table

Below are the contributions of each of our members.

| Name                 | Contribution                                               |
|:---------------------|:-----------------------------------------------------------|
| Emmanuel Ebhohimen   | Model Selection, Model Coding                              |
| Justin Huang         | Data Sourcing and Cleaning, Model Coding                   |
| Gregory Elias        | Model Coding                                               |
| Joshua Abantao       | Data Pre-processing                                        |
| Andrew Titus         | Results / Evaluation and Analysis                          |
