# Twitch-Analysis
Contents of this Repo:
Data Wrangling
Exploratory Data Analysis (aided in great detail by the python library Sweetviz) 
(This may cause some readability issues, I am working on correcting this)
Data pre-processing and Modeling. 
A Slide Deck, with Key Findings and Summary of Methods (though if you read through all this, it is redundant)
A Detailed Report (this readme can be thought of a TLDR for the report)


The most interesting finding (at least in my opinion):
January is an important month for Twitch viewership. 
Games are most likely to debut in the top 200 in January. And they are more likely to remain in the top 200 if a game debuts in January. By a lot. 
I have not been able to come up with a satisfactory explanation for this phenomenon. The best I can come up with at this point is Holidays? (shrugs shoulders)

A final note for the reader:
This repo is not the original repo for this project and is primarily a container for a portfolio project. I will update this as there are a few things I want to add/change.

Below is a an abbreviated version of the project. You can also reference the report and presentation files in this repo

Top 200 Games on Twitch; Binary Classification and Regression

Dataset from Kaggle was obtained for the purpose of attempting to predict which games would remain in the top 200 and subsequently how many hours those games would be watched. 

Data cleaning primarily conisisted of removing rows that were one time events that broke into the top 200. These included the RNC, DNC, and gaming conventions. 

Data wrangling included creating a DataFrame that included the games debut month in the Top 200, its associated data, and the hours watched at 1 month, 3 months, and 6 months after its debut month. 

EDA showed that a disporportionate amount of games debuted in January compared to the other months and the games that debuted in January were more likely to remain popular at 1, 3, and 6 months. 

Modeling showed this to be a useful feature. 

Random Forest Classifier and Logistic Regression were compared to predict which games would remain in the top 200. Random Forest Classifier performed slightly better on its ROC curve 1 month after debut

These both performed better than baseline. 

The baseline took the proportion of games that remained in the top 200 and used that as percentile. The top games by hours watched up until that percentile were predicted to remain in the top 200 games. 

This was repeated for 3 months after debut, but keeping the hours watched at 1 month as a feature. Again the models were more accurate than baseline. 

At 6 months both models and baseline prediction were 100% accurate. Basically games that were popular at 3 months were gauranteed to be popular for at least another 3 months. 

A regression analysis was performed using Multiple Linear Regression and Random Forest Regressor. 

These were compared with two baselines: 1) predicting that the hours watched at 1 month after debut would be the hours watched in the debut month. 

2) A median adjusted version of 1

The Multiple Linear Regression performed about equal to baseline and the Random Forest Regressor performed better. 

This held for the 3 month data as well. (Using 1 month hours watched as the baseline and median adjusted baseline)

At 6 months the 3 month the hours watched baseline outperformed both models 




