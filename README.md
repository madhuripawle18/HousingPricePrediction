# Housing Price Prediction

![Website.png]
## Research Question

Exploratory data analysis (EDA) will be used to visualize imporant trends in the data. EDA will also provide input into the need for feature pre-processing such as dimensionality reduction, null handling and feature scaling. The pre-processed data (pertinent features) will be used to analyze the research question: Will it rain tomorrow?

## Source & Domain

* Domain: Weather forecasting. Precisely to predict whether it will rain tomorrow or not?

* Source: Kaggle, https://www.kaggle.com/jsphyg/weather-dataset-rattle-package

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

## Tentative Plan

### Load data onto BigQuery
After observing the column in the dataset and their importance in order to predict if it will rain tomorrow or not, we have to do the data pre processing and cleaning the data. Selecting the features from dataset that effect the model. 

![Load Data in BigQuery.png](https://github.com/madhuripawle18/KBS-Project/blob/master/images/Data%20in%20BigQuery.png)

### Exploratory Data Analysis and Data Preprocessing using AI Platform
This part of the project will involve visualizing the dataset based on different features from the dataset.Creating graphs that analyze the importance of the columns.Distribution graph inferes observation on different locations according to the dataset. 

**The below image shows the correlation between each variable in the Australian Weather Dataset**
![Image of Heatmap.png](https://github.com/madhuripawle18/KBS-Project/blob/master/images/Heatmap.png)

**The below image shows the correlation between numerical variables in the Australian Weather Dataset**
![Image of Pairplot.png](https://github.com/madhuripawle18/KBS-Project/blob/master/images/Pairplot.png)

**The below image shows the boxplots used to detect outliers in the Australian Weather Dataset**
![Image of Boxplot_to_detect_Outliers.png](https://github.com/madhuripawle18/KBS-Project/blob/master/images/Checking%20for%20Outliers.png)

### Dashboard for Data Engineers
Visualize numerical and categorical data in Data Studio for EDA.
![Image of Data_Engineer_Dashboard.png](https://github.com/madhuripawle18/KBS-Project/blob/master/Dashboards/Data%20Engineer%20Dashboard.png)


### Train Logistic Regression Model on the dataset.
Creating Logistic Regression model and running the model on the dataset help to predict the output variable with high accuracy.

![Model in BigQuery 1.png](https://github.com/madhuripawle18/KBS-Project/blob/master/images/Logistic%20Regression%20Model%20in%20BigQuery%201.png)
![Model Data in BigQuery 2.png](https://github.com/madhuripawle18/KBS-Project/blob/master/images/Logistic%20Regression%20Model%20in%20BigQuery%202.png)

### Make predictions using the testing data

![Predictions.png](https://github.com/madhuripawle18/KBS-Project/blob/master/images/Predictions.png)

### Evaluation of results using  accuracy, precision, recall, f1-score and roc curve

![Evaluate Model.png](https://github.com/madhuripawle18/KBS-Project/blob/master/images/Model%20Evaluation.png)
