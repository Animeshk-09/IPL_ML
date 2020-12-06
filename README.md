# Creating a IPL Dream team
## Data collection 
The data was downloaded from kaggle. 
ipl_new.ipynb - this file processes the 2 csv(matches and deliveries) files provided into meaningful data, analysis, insights and a predictive model

##Our Objective here
1.Top Batsmen and their performance metrics
2.Top Bowlers and their performance metrics
3.Build a model to predict the winner of an IPL match

##Libraries required for running the program:
Data Processing - pandas, numpy, datetime, joblib, timeit
Data Visualization - matplotlib.pyplot, seaborn
Folder Operations - pathlib
Modeling - sklearn (model_selection, linear_model, tree, ensemble, neural_network, pipeline, preprocessing, impute, metrics, decomposition)

##Creating some of the features for analyzing:
1.mapping names of various categories,
2.Batting performance metrics such as batting averages, strike rates, top performances - 200s, 100s, 50s etc., boundary_rate, farm_rate, dot_rate, comparison across multiple time periods (i.e. all 12 seasons, the last 3 seasons or just the last 1 year)
3.Bowling performance metrics such as bowling averages, strike rates, top performances - No. wickets in a match, comparisons across time periods etc.
4.Each Innings was divided into 4 quarters to see how momentum plays a part in victories

##Batting Performances
###Batting performances were analyzed to identify
1.The top 10 run-makers were identified
2.Features such as Batting Strike Rates, Batting Economy Rates
3.Who is the most valuable batsman in the IPL?
4.Batsmen were analyzed along multiple parameters
5.Batting performances were then analyzed over other time periods such as the last 3 years and only 2019 to identify top batsmen

##Bowling Performances
###Bowling performances were analyzed to identify
1.The top 10 wicket-takers were identified
2.Features such as Bowling Strike Rates, Bowling Economy Rates
3.Bowlers were analyzed along multiple parameters
4.Is Malinga the best bowler in the IPL?
5.Bowling performances were then analyzed over other time periods such as the last 3 years and only 2019 to identify top batsmen

##Fielding Performances
1.Similarly players with the most catches, stumpings and run-outs were then idenified

##A model was then built to predict a winner in a match
###To determine the best model
1. 5 different classifiers were used
-Logistic Regression
-Decision Tree
-AdaBoost
-RandomForest
-MultiLayerPerceptron

2. These models were put through a Pipeline with the following steps:
-Simple Imputer to impute values to NaN
-Standard Scaler to scale the values
-PCA to reduce the variables to principal components that explain over 99%
-Classifier was then grid searched to get the right model hyper parameters

3. The models were then saved as pickle files
