# CITC_Task
Cars price prediction 

This repo is for a job offer coding task and the task was as follow:

``` You need to build a model that predicts the price of the car using Python. Please make sure to use at least 3 different methods/algorithms to predict the price and report which one will be most accurate. ```


## Dataset:
the dataset contains 8 features 301 row
  1. Car Name: Nominal
  
  Missing | Unique
------------- | -------------
1 | 47

  2. Year: Numeric
  
  Min | Max | Mean | StdDev 
------------- | ------------- | ------------- | -------------
2003 | 2018 | 2013 | 2.891

  3. Mileage: Numeric
    
  Min | Max | Mean | StdDev 
------------- | ------------- | ------------- | -------------
500 | 500000 | 36947.206 |	38886.884

  4. Fuel type: Nominal
  
  Label | Count
------------- | -------------
Petrol | 239  
Diesel |	60
CNG |	2	

  5. Seller Type: Nominal
    
  Label | Count
------------- | -------------
Dealer | 195  
Individual |	106

  6. Transmission type: Nominal
    
  Label | Count
------------- | -------------
Manual | 261  
Automatic |	40

  7. Previous owners: Numeric
      
  Min | Max | Mean | StdDev 
------------- | ------------- | ------------- | -------------
0 | 1 | 0.043 |	0.248
  
  8. Selling price: Numeric
      
  Min | Max | Mean | StdDev 
------------- | ------------- | ------------- | -------------
0.1 | 35 | 4.643 |	5.081

Bellow a histogram for all  features

![histogram](https://github.com/HebahAlshamlan/CITC_Task/blob/master/img/Histogram.JPG)

## Preprocessing
  - Remove Outliers
  - Fill the Missing value
  - Convert to numeric representation
  - Add new features
  - Handel Car's name
  - Feature selection

## Correlation matrix

![Correlation matrix](https://github.com/HebahAlshamlan/CITC_Task/blob/master/img/download%20(2).png)

## Models
 - Shallow learning (Machine Learning)
    - Linear regression
    - Random forest regressor
    - Support vector regression
  - Deep learning
    - CNN
      - Baseline model
      - Standardizing Dataset
      - Tuning the network

## Conclusion

|Preprocessing| Models | MSE  | R2  | RMSE | Mean |
| :---:   | :---:   | :-: | :-: |:-: |:-:  |
|Without Names| LR | 4.096 | 0.668 |  4.096 | |
|One-Hot-Encoding|LR|4.105|0.731|4.105| |
|Without Names| RFR| 4.205 | 0.660 | 4.205  | |
|One-Hot-Encoding| RFR| 2.723  | 0.821 | 2.723 | |
|Without Names| SVM| 12.037 | -0.026 | 0.026  | |
|One-Hot-Encoding| SVM | 15.883 | -0.042 | 15.883 | |
|One-Hot-Encoding|  CNN| 22.26 |  |   | -27.59 |
|One-Hot-Encoding| CNN | 4.91 | | | -4.05|
|One-Hot-Encoding|  CNN| 5.26 |  |   | -4.19|

As we can see the Random Forest Regression gives a high R2 score **82%** with Mean square error 2.723 that is mean it is the closest to the line best fit.

## Visualizations Excerpts

![](https://github.com/HebahAlshamlan/CITC_Task/blob/master/img/RFR%20plot.png)

**The plot of the Random forest regressor model which achieved the highest accuracy**

![](https://github.com/HebahAlshamlan/CITC_Task/blob/master/img/pred-RFR.png)

**Graph shows predictions VS the actual which miss the actual values at some places**

![](https://github.com/HebahAlshamlan/CITC_Task/blob/master/img/RMSE.png)

**R-Squared & RMSE by number of features**

## The jupyter notebook has the following sections:
- Libraries
- Load dataset
- Exploratory Data Analysis
   - Selling price
   - Convert to numeric representation
   - Missing values
      - year
      - Mileage
      - Care Name
  - Feature Extraction
      - Correlation matrix
- Split the data (training\testing)
- Models
  - Shallow Learning (ML)
    - Linear regression
      - Feature Selection using RFE & K-Fold Cross Validation
    - Random force Regressor
      - Feature Selection using RFE & K-Fold Cross Validation
    - Support vector regression
  - Deep learning
    - CNN
- Conda setup

