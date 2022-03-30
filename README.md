#MoneyBall

The MoneyBall project consisted of using Python to build predictive models for whether or not a team will make the playoffs that given year based off different statistics. Over the last 6 weeks this data was cleaned, organized, and analyzed to make sure of proper performance of the analytical process.

The different models that were used to review this information were a RandomForest Model, KNeighborsRegressor Model, BaggingRegressor Model, and a DecisionTree Model. Between the 4 Models the one that performed the best was the RandomForest Model. Below you will find the scores of each and their scores after manipulating the hyperparameters:

#Default Random Forest Model Evaluation:

- RF Training RMSE: 0.09532412240187849
- RF Testing RMSE: 0.2580364164372777
------
- RF Training MAE: 0.20667958345334989
- RF Testing MAE: 0.3370517706583013
------
- RF Training R2: 0.9432542413049043
- RF Testing R2: 0.5700558164862841

#Hypertuned Random Forest Model Evaluation:

- RF_GS Training RMSE: 0.21924717649978334
- RF_GS Testing RMSE: 0.25936402429469196
------
- RF_GS Training MAE: 0.3252794026835862
- RF_GS Testing MAE: 0.3483081794040972
------
- RF_GS Training R2: 0.6998102950546445
- RF_GS Testing R2: 0.5656202746214216

#Default KNeighborsRegressor Model Evaluation:

- KNN Training RMSE: 0.22215006043359375
- KNN Testing RMSE: 0.2835306163179038
------
- KNN Training MAE: 0.3269960350316299
- KNN Testing MAE: 0.3839304590711675
------
- KNN Training R2: 0.6918085067476136
- KNN Testing R2: 0.48090123204683133

#Hypertuned KNeighborsRegressor Model Evaluation:

- KNN_GS Training RMSE: 0.22215006043359375
- KNN_GS Testing RMSE: 0.2835306163179038
------
- KNN_GS Training MAE: 0.3269960350316299
- KNN_GS Testing MAE: 0.3839304590711675
------
- KNN_GS Training R2: 0.6918085067476136
- KNN_GS Testing R2: 0.48090123204683133

#Default BaggingRegressor Model Evaluation:

- BAGREG Training RMSE: 0.10999803225315942
- BAGREG Testing RMSE: 0.27261361267952455
------
- BAGREG Training MAE: 0.2091003197581097
- BAGREG Testing MAE: 0.3461288702278312
------
- BAGREG Training R2: 0.9244390154701386
- BAGREG Testing R2: 0.5201061874617112

#Hypertuned BaggingRegressor Model Evaluation:

- BAGREG_GS Training RMSE: 0.24481462197793483
- BAGREG_GS Testing RMSE: 0.27544533009315997
------
- BAGREG_GS Training MAE: 0.3452836214198108
- BAGREG_GS Testing MAE: 0.36055512754639896
------
- BAGREG_GS Training R2: 0.6257149486157335
- BAGREG_GS Testing R2: 0.5100848138315976

#Default DecisionTree Model Evaluation:

- DECTREE Training RMSE: 0.0
- DECTREE Testing RMSE: 0.34188172937891387
------
- DECTREE Training MAE: 0.0
- DECTREE Testing MAE: 0.34188172937891387
------
- DECTREE Training R2: 1.0
- DECTREE Testing R2: 0.24525219522156416

#Hypertuned DecisionTree Model Evaluation:

- DECTREE_GS Training RMSE: 0.24573621425166406
- DECTREE_GS Testing RMSE: 0.27610234305612574
------
- DECTREE_GS Training MAE: 0.347523486960924
- DECTREE_GS Testing MAE: 0.3654821423817536
------
- DECTREE_GS Training R2: 0.6228916902664601
- DECTREE_GS Testing R2: 0.5077448611816449

At first glance when finding the r2 values it was 1.0 training score, and 0.19 testing score. But after manipulating the hyperparamters and finding out the best score for this model would be at a max depth of 5 there is a night and day difference. After setting the hyperparamters to a max depth of 5, there is a training score of 60% and a testing score of 59%. Although there is a slight difference between the training and testing scores, the training score for the r2 value is slightly higher than the testing score which means that the data was not overfit. The RMSE training score was 1.607 and for testing was 1488.

The overall goal of this project is to help predict different ways to help with Outlet Sales. The recommendation is to focus on Item MRP, and Item Visibility, Outlet Type, Outlet Size, and Item Type to help increase Outlet Sales. For instance, having more attention and focus on specific items that have a low visibility but higher sales should be the main focus so you are able to fit more items on shelves.
