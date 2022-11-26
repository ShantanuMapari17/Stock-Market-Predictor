# Stock-Market-Predictor
Objective of this project is to analyze the effect of adding some generality in building a stock price predictor for a seleciited stock by adding data of other stocks in model training while using a correlation coefficient to adjust their impact in learning the model weights

## Selection of Stocks
12 Stocks are selected, 3 stocks from each of the sectors in banking, healthcare, information technology and Energy sector to keep a balanced effect of correlation from various categories of companies. 1 stock from these 12 is selected as the target stock for which price predictions will be focused on. 
i.e
SBIN HDFCBANK AXISBANK
SUNPHARMA DRREDDY CIPLA
INFY WIPRO TCS
BPCL COALINDIA POWERGRID

## Feature Generation
Instead of using standard features of open and close values of stocks, we are going to use custom built features which are itself predictions from some basic price prediction models. 2 methods of feature generation that we have used are :
  -Linear regression with variable degrees
  -Curve similarity with varying curve length
 
## Model Creation
We have used RNN + LSTM for training of time series price prediction model. We will first train a specialized model for predicting the prices of the target stock. Once we are sure that we have achieved the best results possible, we will then train a generalized model by using data of various stocks along with their correlation factors.

### Correlation Betwn Stocks
![correlation_bw_SBI AXIS INFY_200](https://user-images.githubusercontent.com/40542049/204107690-7729d41c-fa68-4c0c-96f4-a769f258fd12.png)

### Generalized Loss
![BS256_E50_New_SUM](https://user-images.githubusercontent.com/40542049/204107727-901f5a20-7ebc-49cd-b660-ec393bb5d687.png)

### Prediction 
![generalized_test_predictions_bs256_e50_1 3](https://user-images.githubusercontent.com/40542049/204107834-2d7dc164-99b0-410c-bf6a-5597e8013525.png)
