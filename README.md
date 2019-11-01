# airline_classifcationproject

Mod_5 Classification project 

https://docs.google.com/presentation/d/1C3j3M1RD1broGEBP-hSPHpQul_8n4n7t/edit#slide=id.p1


**Question**
Can we predict if a flight will be delayed?
(The US department of transportation defines a delayed flight as 15 minutes or more past the departure scheduled time.)

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

**Evaluation Data Analysis**
My target variable is somewhat evenly distributed as you can see in the image below. 

http://localhost:8888/view/CourseMaterials/Projects/Project_4_classification/airline_classifcationproject/target_image.png

You can clearly see that there are differences between months with delayed flights. 

![](/airline_classifcationproject/monthly_delays.png)

