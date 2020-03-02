# Airline Classification Project

**Can we predict if a flight will be delayed?**
(The US department of transportation defines a delayed flight as 15 minutes or more past the departure scheduled time.)

***Presentation:***
https://docs.google.com/presentation/d/1C3j3M1RD1broGEBP-hSPHpQul_8n4n7t/edit#slide=id.p1

Classification Project Lifecycle
1. State the question and determine required Data
2. Clean_data = Acquire the data in an accessible format
3. Evaluating_data = Identify and correct missing data points/anomalies as required
4. Evaluating_data = Prepare the data for the machine learning model  
5. Modeling= Establish a baseline model that you aim to exceed
6. Modeling= Train the model on the training data
7. Make predictions on the test data
8. Compare predictions to the known test set targets and calculate performance metrics
9. Adjust the model, acquire more data, or try a different modeling technique
10. Interpret model and report results visually and numerically


**Data Cleaning**
Target: Delayed_Flight >= 20%
- Dataset originally had number of flights delayed per month/year for each airport
Features: Months, years, total arrival flights, airports
- Removed flight delay minutes from data set as well as %delays

Remove observations with missing data
Rename columns name
Created Dummy variables
- Month
- Year
- Airport
Scaled data for better performance of models

Note: There was high correlation between the minute features and target variable which can cause issues to the modeling process. (minute delay columns dropped)

**Evaluation Data Analysis**
My target variable is somewhat evenly distributed as you can see in the image below. (no need to smote)

![](target_image.png)

You can clearly see that there are differences between months with delayed flights.

![](monthly_delays.png)


**Model Evaluation**
![](model_eval.png)

As you can see XGBoost preformed the best out of all models.

**XGBoost Statistical Measures**
Accuracy: 79.66%
(highest model)

F1-Score: 80.34%
(highest model)

Precision Score: 79.44%
(highest model)

Recall Score: 81.26
(Sensitivity/TPR)

AUC: 80%
Specificity: 77.98%
FPR: 22.02%

![](XGB_confmatrix.png)

**XGBoost Feature Importances:**

![](XGB_featureimportances.png)
