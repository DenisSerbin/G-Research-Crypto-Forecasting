# G-Research-Crypto-Forecasting
In spring 2022 I participated in the Kaggle competition [G-Research Crypto Forecasting](https://www.kaggle.com/competitions/g-research-crypto-forecasting).

I was doing pretty well in the begining of the testing phase (was holding the 142nd place among about 2000 teams after the first three weeks). But in the later stages of the testing process, as the test data was udpated, either my submissions became too slow, or unexpected errors occured, who knows - Kaggle doesn't give detailed explanations - all my submissions got discarded from the competition.

Here I'm presenting one of my models that generated a decent private score of 0.013 (the competition winner got 0.0326).

## The competition
G-Research provided several datasets containing information on historic trades for several (13) cryptoassets, such as Bitcoin and Ethereum.

The goal was to predict (obviously) future returns of the listed cryptoassets. Submissions were evaluated on a weighted version of the [Pearson correlation coefficient](https://en.wikipedia.org/wiki/Pearson_correlation_coefficient)

## Datasets
The original training dataset is given in three files: 
 - 'train.csv' - contains 1-minute volume, open/close/high/low and volume weighted average price for all 13 assets,
- 'asset_details.csvv' - provides the real name of each cryptoasset and the weight each cryptoasset receives in the metric.
- 'supplemental_train.csv' - contains more 'train.csv'-type data obtained in real time after the competition deadline passes (still can be useful in mean calculations etc.)

The files can be downloaded from the competition page [https://www.kaggle.com/competitions/g-research-crypto-forecasting/data](https://www.kaggle.com/competitions/g-research-crypto-forecasting/data)

## Solution

Pretty simple multilayer perceptron with three hidden layers takes the open/close/high/low and volume weighted average prices for all 13 cryptoassets and
outputs a vector of 13 future returns. As a loss function I took '1 - Pearson correlation coefficient' (see [gresearch-model-2.ipynb](gresearch-model-2.ipynb)
