# Machine Learning Trading Bot
### Johnathan Overton


## Overview of the Analysis

* The purpose of this analysis was to enchance current algorithmic trading systems so as to maintain the firm's competitive advantage by employing a baseline algorithmic model and then test the model against other models.
* The financial information used was based off of the ohlcv.csv with the following dimensions
  * date
  * open
  * high
  * low 
  * close
  * volume

* In this model, the following technologies were incorporated:
  * Jupyterlab Notebook
  * Pandas
  * DateOffset
  * hvPlot
  * ScikitLearn
  * Standard Scaler
  * OneHotEncoder
  * Classification Report

* How to Use
  * Simply clone the repository and execute machine_learning_trading_bot.ipynb

* Machine Learning process stages
  * Establish a Baseline Performance
  * Tune the Baseline Trading Algorithm
  * Evaluate a New Machine Learning Classifier
  * Create an Evaluation Report

## Results

Baseline Classification and Graph

!(https://github.com/Johove83/Algorithmic-Trading/blob/main/Machine%20Learning%20Trading%20Bot/images/baselineclassification.png)

!(https://github.com/Johove83/Algorithmic-Trading/blob/main/Machine%20Learning%20Trading%20Bot/images/baseline.png)

Training Window

!(https://github.com/Johove83/Algorithmic-Trading/blob/main/Machine%20Learning%20Trading%20Bot/images/9monthwindowclassification.png)

!(https://github.com/Johove83/Algorithmic-Trading/blob/main/Machine%20Learning%20Trading%20Bot/images/9monthwindow.png)

SMA

!(https://github.com/Johove83/Algorithmic-Trading/blob/main/Machine%20Learning%20Trading%20Bot/images/fullytunedclassification.png)

!(https://github.com/Johove83/Algorithmic-Trading/blob/main/Machine%20Learning%20Trading%20Bot/images/fullytuned.png)

Logistic Regression

!(https://github.com/Johove83/Algorithmic-Trading/blob/main/Machine%20Learning%20Trading%20Bot/images/lrclassification.png)

!(https://github.com/Johove83/Algorithmic-Trading/blob/main/Machine%20Learning%20Trading%20Bot/images/lr.png)






## Summary

While both Machine Learning models perform exceptionally well, the second model is found to be ideal as it outperforms the first model in both accuracy and precision while losing only a tenth of a percent point in recall.

It is of note that the second model remains consistent in accurately predicting, both, health and high-risk loans.

Therefore it is my recommendation to utilize the second model in credit risk prediction.
