---
layout: default
---

* * *

# Intro / Background

Fantasy football allows fans to manage their own team of players. To compete, fantasy teams earn points based on the performances of their players during real NFL games. However, It is common for players to exceed or underperform compared to their expectations. With a multitude of factors such as injuries, matchup grades, and team strategies, how can one accurately predict player performances? This project aims to address that using the default PPR scoring system.

# Problem / Definition

We aim to predict the rankings/fantasy points for all NFL quarterbacks using machine learning for the upcoming seasion

# Methods Algorithms and Libraries

## Methods

1. Data collection and processing

We downloaded quarterback fantasy statistics from 2019, 2020, 2021, 2022, and 2022 in the form of csv from "https://www.4for4.com/nfl-player-stat-explorer". Here is a snippet of the format and data of each csv file:

![csv ss](/fantasy-football/assets/css/1.png)

After downloading the data in the form of multiple csv files, we loaded the data into our machine learning environment and into separate Pandas dataframes. These 5 separate data frames are then concatenated into a single data frame for processing:


Here is a snippet of the semi-processed data and its column names:

Then, we transformed categorical features using OneHotEncoder, converting categorical variables into a more efficient format that could be provided to ML algorithms to do a better job in prediction. We also used ColumnTransformation to preprocess different subsets of features, and that left numeric features "untransformed" and ensured only the relevent features are included in the model training process. In addition, we used scaling and normalization for our SVR algorithm to improve SVR performance:

 ![Some Picture]({{ site.url }}{{ site.baseurl }}./4.png)

3. Split data set into training and testing data (80/20 split)

We have the dataset for 2019, 2020, 2021, 2022, and 2023, so we decided th use 2019, 2020, 2021, 2022 as training data, and use 2023 as our testing data, hence a 80/20 split. The intention is to use data from previous years to train the model and test it on the most recent year's data

5. Build ML models

We initialized and trained various regression models on the training set. The machine learning models used in this porject include linear regression, ridge regression, lasso regression, random forest, gradient boosting, and SVR:  

Results

As a recap, we used 2019, 2020, 2021, 2022's fantasy data to train a machine learning model, and after constructing the models, we used 2023's fantasy data to test the accuracy of the model. Here is the data predicted by various different machine learning models. For clarity purposes, we placed the predicted data next to 2023's actual data. 


Analysis and Discussion

Here are the graphs that show the relationship between predicted data and actual data using Matplotlib:



As shown, the model relatively accurately predicted the fantasy points for 2023. To further show the relationship between predicted and actual data, we calculated the mean squared error (MSE) for each model:


Which model performs the best? Here is a chart that visualizes the MSE for each model:


As shown, linear regression has the best performance, followed by ridge regression and gradient boosting.


 

[Our Project's Dataset](https://www.4for4.com/nfl-player-stat-explorer).


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
