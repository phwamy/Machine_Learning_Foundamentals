# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Pei-Hsin Wang

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
If there were negative predictions on bike demand, the system would automatically reject the submission. Therefore, before submitting the result, negative numbers should be adjusted to 0.

### What was the top ranked model that performed?
'WeightedEnsemble_L3' was the the best model.

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
Exploratory data analysis helped me to understand the overall trends and characteristics of data and enabled me to interpret trends and importance features for forcasting bike demand.

Few insights:
1. Average Bike Rentals per Month:
    - The trend shows higher bike rentals during the warmer months (May through October) and lower rentals during colder months (November through April), consistent across both years. This indicates a clear seasonal pattern that can be crucial for planning and forecasting.

2. Average Bike Rentals by Day of the Week:
    - Bike rentals are generally higher on weekdays compared to weekends. This pattern may be due to the use of bikes for commuting during workdays.

3. Average Bike Rentals by Hour of the Day:
    - There are peak rental times at around 8 AM and 5 PM, corresponding to typical commuting hours. The low rental activity in the early morning hours indicates minimal usage during late-night hours.
    
<img src="/img/date_analysis.png" alt="date_analysis.png" width="500"/>
    
4. Weather Distribution:
    - Most of the data is recorded during clear weather (Weather 1). The frequency decreases with worsening weather conditions, with very few data points recorded during heavy rain/snow (Weather 4).
    
    


After Exploratory Data Anlaysis (EDA), I have:
- **Feature Reduction**: Dropped `atemp` due to its high correlation with temp, as both variables measure temperature.
- **Outlier Removal**: Excluded outliers in the `humidity` and `windspeed` data, which potentially represented inaccurate measurements or extreme conditions. This removed 248 datapoints from the original 10,886, leaving 10,638. These changes aim to enhance model reliability and generalization by focusing on more typical data conditions.
- **Transform Date**: Transforming datetime into new categorical features: 'year', 'month', and 'hour'.
- **Create Dummy Data**: Convert categorical data into dummy columns that returns 47 columns in total features.

### How much better did your model preform after adding additional features and why do you think that is?
TODO: Add your explanation

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
TODO: Add your explanation

### If you were given more time with this dataset, where do you think you would spend more time?
TODO: Add your explanation

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|?|?|?|?|
|add_features|?|?|?|?|
|hpo|?|?|?|?|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](img/model_test_score.png)

## Summary
TODO: Add your explanation
