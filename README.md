# Predicting Whether or Not Alcohol Was Involved in a Fatal Car Accident

In this project, I downloaded two datasets from kaggle which pertained to fatal car accidents in the year 2015, and used the data to create a classification model to predict whether or not alcohol was a factor in the car accident. Below is a short description of the purpose of each file.

## 2015-traffic-fatalities

This folder contains the datasets which were used to create the models. They were able to be merged on specific case numbers that were unique to each individual crash.

## Clean Data

The data originally starts out with 153 features and close to 50,000 data points, but features that were not indicative of the presence of alcohol were removed, as were data points in which the some of the remaining features had unknowns as values. Some features are added (based on other features), and the final dataframe contains 6 features and about 14,000 data points. The means of the two different categories (drunk and sober) are compared, with categorical features having means that represent the proportion of times that feature would occur.

## Modeling - Class Imbalance

There are clearly more accidents involving sober drivers as opposed to those involving drunk drivers, so this needs to be taken into account (the actual ratio is about 9:2). This is done by testing multiple different types of classification models with multiple different types of oversampling/undersampling. I created functions in order to cross-validate the models as well as test them. The metric used here was F1 scoring. The best model created used X-Gradient Boosting, and features were eliminated by checking the "importance" of them using the xgboost library. Furthermore, different thresholds were tested, with the F1-score being the highest at a 16% threshold (the accuracy was at its near peak here as well).

## Fatal Accidents Presentation

I gave a brief 5-minute presentation on my findings. Tableau was used to create graphs and charts, as well as interactive visuals which were demonstrated during the presentation. These are the slides used to discuss the results.