# Ontario Housing Market Analysis Part 2
This project uses neural networks to create a model that predicts Ontario housing prices. The model is used through an Amazon Lex chatbot that allows the user to pick a region in Ontario and a building type that they are interested in. The chatbot gives the user the option to choose a date for the price as well.

## Contributors
- Jamie Mellway
- Josh Esteban
- Majeed Raheem
- Joey Falvo
- Rafi Nazamodeen

## Background
There are many contributing factors to Ontario's housing market. Housing prices fluctuate due to many market forces making this a regression problem. This project aims to take data that is relevant to the market and create a neural network that can predict the housing prices.

## Dependencies
This project utilizes the following packages:
- [Python 3.10.10](https://www.python.org/)
- [NumPy 1.23.5](https://numpy.org/)
- [pandas 2.0.1](https://pandas.pydata.org/)
- [hvPlot 0.8.3](https://hvplot.holoviz.org/)
- [scikit-learn 1.2.2](https://scikit-learn.org/stable/)
- [TensorFlow 2.12.0](https://www.tensorflow.org/)
- [Keras 2.12.0](https://keras.io/)

## Data
Data was collected and analyzed to create the best model. Altogether, there are 13 features and 161 predictors, each with 176 data points.

### Collection
Actual housing price data was found from CREA. These are our ground truth data that we want to predict. Our feature data was found from various sites covering data that we felt would be relevant to housing prices. These include: Yahoo Finance, Macrotrends, Statistics Canada, and Bank of Canada.

[Lumber Prices](https://www.macrotrends.net/2637/lumber-prices-historical-chart-data)    
[iShares Global Timber & Forestry ETF](https://finance.yahoo.com/quote/WOOD/history?p=WOOD)    
[SPDR S&P Homebuilders ETF](https://finance.yahoo.com/quote/XHB/history?p=XHB)   
[iShares U.S. Home Construction ETF](https://finance.yahoo.com/quote/ITB/history?p=ITB)    
[Consumer Price Index](https://www150.statcan.gc.ca/t1/tbl1/en/tv.action?pid=1810000601&cubeTimeFrame.startMonth=12&cubeTimeFrame.startYear=2005&cubeTimeFrame.endMonth=04&cubeTimeFrame.endYear=2023&referencePeriods=20051201%2C20230401)    
[Interest rates](https://www.bankofcanada.ca/rates/interest-rates/canadian-interest-rates/) 

### Analysis
Some data from our CPI set was duplicate, didn't add any value and led to overfitting. We isolated the data and removed it from our set.
Removed data:
- All-items 8
- All-items excluding food
- All-items excluding food and energy

## Description
The neural network used to create the model has the following characteristics:

### Parameters
![Model3 Neural Network](https://github.com/JamieMellway/FintechBootcampProject2/blob/main/Images/Model3_nn.png)

### Evaluation
|Metric|Value|
|:---|---:|
|R-Squared (train)|0.9974559414984706|
|R-Squared|0.988579310366157|
|Mean Absolute Error|0.06405685077016317|
|Mean Absolute Percentage Error|24.720600483659982|
|Mean Squared Error|0.010621614314503598|
|Root Mean Squared Error|0.1030612163449646|

### Graphical Results
![Model3 Neural Network](https://github.com/JamieMellway/FintechBootcampProject2/blob/main/Images/actual_and_predicted_model3.png)

## Usage
The user can interact with an Amazon Lex chatbot that will give them the price of a house in their desired location and building type for a given date. Also, the python notebooks can be run as is, to create the model and make predictions.