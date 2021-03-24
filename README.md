# Housing Price Prediction

![Website.png](https://github.com/madhuripawle18/HousingPricePrediction/blob/main/Website.png)

## About the Dataset

* This dataset contains about 10 years of daily weather observations from numerous Australian weather stations.

* It consists of 24 columns and 142193 rows. It has numerical, categorical and boolean data.

* It is an unbalanced dataset, as the target column RainTomorrow has 110316 "No" entries and 31877 "Yes" entries.


## Target Audience

The target audience would be the general public of respective areas in Australia. The dataset consists of 49 locations so people living in those 49 locations can have the benifit of knowing if it will rain the next day or not and plan their day accordingly.

## Data Preprocessing

The data cleaning steps that we are going to follow are :
* Make sure the datatypes are correct.
* Drop the columns that have less than 60% of data.
* Drop rows that consist of missing values in any of the columns.
* Handle outlier using top-coding approach.
* Encode Categorical data using One Hot Encoding as Logistic Regression cannot handle categorical data.


## Train Linear Regression Model on the dataset.


## Evaluation of results using  accuracy, precision, recall, f1-score and roc curve

