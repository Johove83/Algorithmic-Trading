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

### Baseline Classification and Graph

![1](https://github.com/Johove83/Algorithmic-Trading/blob/main/Machine%20Learning%20Trading%20Bot/images/baseline/baselineclassification.png)

![2](https://github.com/Johove83/Algorithmic-Trading/blob/main/Machine%20Learning%20Trading%20Bot/images/baseline/baseline.png)

This model determines a 43% accuracy at -1.0 and 56% at 1.0 signals.
The strategy return was predicted to be 1.5 and the actual returns were about 1.38.

### Training Window Increased From 3 to 9 Months

![3](https://github.com/Johove83/Algorithmic-Trading/blob/main/Machine%20Learning%20Trading%20Bot/images/ninemonth/9monthwindowclassification.png)

![4](https://github.com/Johove83/Algorithmic-Trading/blob/main/Machine%20Learning%20Trading%20Bot/images/ninemonth/9monthwindow.png)

Increasing the training window from to 9 months did not seem to offer any change in the classification report.

However, strategy returns and actual returns increased to 1.61 and 1.6, respectively.

### SMA Tuning

![5](https://github.com/Johove83/Algorithmic-Trading/blob/main/tuned/Machine%20Learning%20Trading%20Bot/images/fullytunedclassification.png)

![6](https://github.com/Johove83/Algorithmic-Trading/blob/main/tuned/Machine%20Learning%20Trading%20Bot/images/tuned/fullytuned.png)

The short window was increased from 4 days to 20 days.
The long window was increased from 100 days to 115 days.



Logistic Regression

![7](https://github.com/Johove83/Algorithmic-Trading/blob/main/Machine%20Learning%20Trading%20Bot/images/lrclassification.png)

![8](https://github.com/Johove83/Algorithmic-Trading/blob/main/Machine%20Learning%20Trading%20Bot/images/lr.png)






## Summary

While both Machine Learning models perform exceptionally well, the second model is found to be ideal as it outperforms the first model in both accuracy and precision while losing only a tenth of a percent point in recall.

It is of note that the second model remains consistent in accurately predicting, both, health and high-risk loans.

Therefore it is my recommendation to utilize the second model in credit risk prediction.
