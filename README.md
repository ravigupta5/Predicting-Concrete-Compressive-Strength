# Predicting-Concrete-Compressive-Strength
### Applying domain knowledge to improve prediction accuracy

The project involves creating model(s) that will try to accurately predict the compressive strength of concrete. Since we are predicting a continuous variable, it is a regression problem.

### Data Set Information:

The data has been sourced from UCI Machine Learning Repository: http://archive.ics.uci.edu/ml/datasets/concrete+compressive+strength
- Number of instances 1030
- Number of attributes 9
- 8 quantitative input variables (features)
- First 7 features are the constituents of conrete mix (in kg/m3) while the 8th one is the duration in days after which compressive strength test has been performed
- 1 quantitative output variable (compressive strength)
- Missing attribute values: none


## The notebook is divided into two parts:

*Part A: Predicting strength using the raw data as it is

*Part B: Predicting strength after attempting feature engineering

## PART A
- Since all the variables are numerical and there is no missing values, no feature engineering is involved
- Basic exploratory data analysis done
- Predictions made using four different algorithms

![alt text](https://github.com/ravigupta5/Predicting-Concrete-Compressive-Strength/blob/master/parta_rmse.PNG?raw=true)



## PART B
- Applying models after attempting feature engineering
- In part B, the aim is to improve the accuracy of prediction models by using domain knowledge
- Following feature (properties of concrete were introduced/modified) to attain better predictions:
  - **water/cement weight ratio (w/c)** As per Abram's law there is inverse relation between w/c ratio and strength
  - **binders** (cement, fly-ash and slag collectively act as binders)
  - **using only the data with age less than or equal to 28 days** IS-456 (Indian Standard Code for concrete design) recommends concrete testing after 3, 7 and 28 days
  ![alt text](https://github.com/ravigupta5/Predicting-Concrete-Compressive-Strength/blob/master/w_c_ratio.jpg?raw=true)
  
  ## Conclusion
  By introducing feature engineering better predictions are obtained from models
  ![alt text](https://github.com/ravigupta5/Predicting-Concrete-Compressive-Strength/blob/master/partb_rmse.PNG?raw=true)
