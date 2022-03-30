MoneyBall

The MoneyBall project consisted of using Python to build predictive models for whether or not a team will make the playoffs that given year based off different statistics. Over the last 6 weeks this data was cleaned, organized, and analyzed to make sure of proper performance of the analytical process.

The different models that were used to review this information were a RandomForest Model, KNeighborsRegressor Model, BaggingRegressor Model, and a DecisionTree Model. Between the 4 Models the one that performed the best was the RandomForest Model. 

At first glance when finding the r2 values it was 0.92 training score, and 0.57 testing score which shows that there is high variance in the data and is overfit. But after manipulating the hyperparamters and finding out the best score for this model would be at a max_depth of 3, min_samples_split of 2, and n_estimators at 600 there is a major difference. After setting the hyperparamters there is a training score of 69% and a testing score of 56%. The training score for the r2 value is slightly higher than the testing score which means that the data was not overfit.

The overall goal of this project is to help predict whether or not a team will make the Playoffs. The feature columns that are taken into consideration are League, Year, RunsScored, RunsAllowed, Wins, OnBasePercentage, SluggingPercentage, Batting Average, and GamesPlayed. With the target columns being whether or not the team made the Playoffs


Below you will find the scores of the Default Model Evaluation for RandomForest and the Hypertuned Model for RandomForest:

Default Random Forest Model Evaluation:

- RF Training RMSE: 0.09532412240187849
- RF Testing RMSE: 0.2580364164372777
------
- RF Training MAE: 0.20667958345334989
- RF Testing MAE: 0.3370517706583013
------
- RF Training R2: 0.9432542413049043
- RF Testing R2: 0.5700558164862841

Hypertuned Random Forest Model Evaluation:

- RF_GS Training RMSE: 0.21924717649978334
- RF_GS Testing RMSE: 0.25936402429469196
------
- RF_GS Training MAE: 0.3252794026835862
- RF_GS Testing MAE: 0.3483081794040972
------
- RF_GS Training R2: 0.6998102950546445
- RF_GS Testing R2: 0.5656202746214216
