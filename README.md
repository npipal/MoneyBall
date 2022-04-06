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




Below you will find different visuals exploring the data:


![HeatMap MoneyBall](https://user-images.githubusercontent.com/97055926/160735407-02a13ae3-3313-431d-b08a-b4a56341d6ba.png)


There is a strong relationship between our Playoff(target) with a couple of features being RunScored, Wins, OnBasePercentage, SluggingPercentage, and Batting Average.
There is also a strong relationship between the features of the dataset being RunScored, Wins, OnBasePercentage, SluggingPercentage, and Batting Average.


![Runs Scored](https://user-images.githubusercontent.com/97055926/160735636-5ee65c0e-dc8b-42b9-b830-101a0eefb0d9.png)


There are a couple of outliers in this data for RunsScored but everything is plausible. The outliers that are above 950 are a good bet to most likely be teams that do in fact make the playoffs. The outliers that are below 500 are teams that more than likely do not make the playoffs.


![Wins](https://user-images.githubusercontent.com/97055926/160735669-1131aa4e-e39d-49b1-b415-0db83691ef7a.png)


There are a couple of outliers in the data for Wins but everything is plausible. Outliers that are above 100 are teams that more than likely made the playoffs since they play a total of 162 games in the regular season. The outliers that are below 50 are teams who most likely did not make the playoffs. 


![OBP](https://user-images.githubusercontent.com/97055926/160735691-a758641d-bfd6-40dc-9168-14dd406ce6e9.png)

There are some outliers in the data for OnBasePercentage but everything is plausible. OUtliers that are above .36 are teams who more than likely did make the playoffs. The outliers that are below .30 are teams who more than likely did not make the playoffs.


![SLG](https://user-images.githubusercontent.com/97055926/160735228-f9902adc-d0b7-453c-8475-ec6346fb553a.png)


There are a couple of outliers in the data for SluggingPercentage but everything is plausible. Outliers that are above .475 are teams who more than likely made the playoffs. The outliers that are below .325 are teams who more than likely do not make the playoffs. 


![BA](https://user-images.githubusercontent.com/97055926/160735731-4b5de40e-63e9-40e3-80eb-421ab4100887.png)

There are some outliers in the data for BattingAverage but everything is plausible. Outliers that are above .290 are teams who more than likely make the playoffs. The outliers that are below .230 are teams who more than likely did not make the playoffs.


![BASLG1](https://user-images.githubusercontent.com/97055926/162072557-8e7803e2-f3d7-4391-a5ae-405ae1e8037e.png)

After viewing the graph above we can see that teams who have a higher batting average and slugging percentage more often that not have a better chance of making the playoffs. Although there are a few outliers in this case there are teams who did not make the playoffs with a high BA and SLG as well as teams who did make the playoffs with a low BA and SLG.


![RSOBP1](https://user-images.githubusercontent.com/97055926/162072612-1cae9985-4d46-4bbe-b0d1-9309e8e6c04b.png)

After examining the graph we can see that teams who have a higher on-base percentage and total runs scored for the year are more than likely going to make the playoffs that given year. Although we do see some outliers on both sides where teams who did make the playoffs but did not score a lot of runs and had a low on base percentage. As well as teams who did not make the playoffs who scored a lot of runs and had a high on-base percentage.
