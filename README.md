# Machine_learning_trading_bot
This Jupyter notebook application uses supervised machine learning models for algorithmic stock trading predictions using training and testing subsets of historical data. A baseline performance is obtained using fast and slow SMA windows as features with a support vector machines model. This model is tuned by expanding the training subset and adjusting the fast SMA window, and the performance compared using cumulative product of actual vs. strategy returns. Lastly, an adaptive boosting machine learning model is generated for the same data, and evaluated for performance.  

![Cumulative return plot for baseline support vector machines model using fast and slow SMAs](baseline_svm_model)

The baseline support vector machines model using fast (4 days) and slow (100 days) SMA features does not perform well compared to the actual returns or a trading strategy of buy/sell based on previous day's percent change (positive/negative). 

![Cumulative return plot for svm model tuned by extending training data](tune_by_extending_training_data)
![Cumulative return plot for svm model tuned by adjusting fast SMA window](tune_by_adjusting_fast_SMA_window)
![Cumulative return plot for adaptive boosting model](adaptive_boosting_model)

# Summary evaluation report
Tuning the baseline machine learning model by extending the training data from 4 to 8 days produced the best results, although the predictions were still substantially divergent from the actual returns. The adaptive boosting machine learning algorithm performed better than the baseline support vector machines model, and perhaps could be improved by similar tuning strategies. Overall, machine learning does not appear to provide good predictive signals for a day trading strategy. The cumulative return plots for the tuning strategy of adjusting the fast SMA window were identical to the baseline model plots, and both suffered from a lack of precision matching buy signals to positive percent change in the closing stock prices. In contrast, the best performing models, tuning the SVM model with an extended training period, and the adaptive boosting model, had similar precision for buy and sell signals. 

## *Technologies*
This application is written using Python 3.9.7 and uses historical stock trading data (OHLCV - open, high, low, close, volume).

## *Installation Guide*
Install the pandas, numpy, matplotlib and sklearn libraries.

## *Usage*
Run the program from the command line as 'machine_learning_trading_bot.ipynb'.

## *Contributors*
This program was written by David Hockenbery with the assistance of the UW FinTech class of 2021 and instructors. Contact David at dhockenb@gmail.com.

## *License*
opyright (c) [2022] [David Hockenbery]