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

Increasing the training window from to 9 months offered a slight a 2% and 1% accuracy improvement, respectively, for -1.0 and 1.0 signals.

Strategy returns and actual returns increased to 1.61 and 1.6, respectively.

### SMA Tuning (Fully Tuned)

![5](https://github.com/Johove83/Algorithmic-Trading/blob/main/Machine%20Learning%20Trading%20Bot/images/tuned/fullytunedclassification.png)

![6](https://github.com/Johove83/Algorithmic-Trading/blob/main/Machine%20Learning%20Trading%20Bot/images/tuned/fullytuned.png)

The short window was increased from 4 days to 20 days.
The long window was increased from 100 days to 115 days.

The accuracy for the -1.0 signal remained at 45% and the 1.0 signal increased slightly to 57%. Of note, the recall for the -1.0 signal dramastically lowered. Predicted returns dropped to 1.1. However, the actual returns broached 1.8



### Logistic Regression

![7](https://github.com/Johove83/Algorithmic-Trading/blob/main/Machine%20Learning%20Trading%20Bot/images/lrclassification.png)

![8](https://github.com/Johove83/Algorithmic-Trading/blob/main/Machine%20Learning%20Trading%20Bot/images/lr.png)

Compared to the baseline model, the logistic regression model had slightly improved accuracy at the -1.0 signal. The predicted strategy return was lower at 1.1 which is arbitrary as the actual returns were slightly improved at 1.4 making the logistic regression model slightly preferable to the baseline model.

However, the logistic regression model paled in comparison to a fully tuned model. The fully tuned model offered a 1% increase in accuracy at both the 1.0 and -1.0 signals.

Of greater note is that the fully tuned model offered comparable predicted returns and far outperformed the logistic regression model in actual returns.

## Summary

Most interestingly, the fully tuned model offered superior accuracy at both signals. Despite being ranked fairly low for predicted returns, backtesting proves that this model actually offered the greatest actual returns.

A summary consideration would be that, in spite of lower predictions, the fully tuned model offered superior buy and sell signals which resulted in the greatest overall gains.

Therefore it is my recommendation to utilize the model offering a 9 month training window with 20 and 115 days short and long windows, respectively.
