# G-Research-Crypto-Forecasting
In spring 2022 I participated in the Kaggle competition [G-Research Crypto Forecasting](https://www.kaggle.com/competitions/g-research-crypto-forecasting).

I was doing pretty well in the begining of the testing phase (was holding the 142nd place among about 2000 teams after the first three weeks). But in the later stages of the testing process, as the test data was udpated, either my submissions became too slow, or unexpected errors occured, who knows - Kaggle doesn't give detailed explanations - all my submissions got discarded from the competition.

Below I'm presenting one of my models that generated a decent private score of 0.013 (the competition winner got 0.0326).

## The competition

G-Research provided several datasets containing information on historic trades for several cryptoassets, such as Bitcoin and Ethereum. 

The goal was to predict (obviously) future returns of the listed cryptoassets.

## Datasets
The original training dataset is given in three files: 
 - 'train.csv' - contains 1-minute candlesticks (open/close/high/low prices) for all the assets,
- 'asset_details.csvv' - provides the real name of each cryptoasset and the weight each cryptoasset receives in the metric.
- 'supplemental_train.csv' - contains more candlestick data obtained in real time after the competition deadline passes (still can be useful in mean calculations etc.)

The files can be downloaded from the competition page [https://www.kaggle.com/competitions/g-research-crypto-forecasting/data](https://www.kaggle.com/competitions/g-research-crypto-forecasting/data)
