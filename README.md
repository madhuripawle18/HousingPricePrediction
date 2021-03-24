# Housing Price Prediction

![Website.png](https://github.com/madhuripawle18/HousingPricePrediction/blob/main/Website.png)

## Technologies Used 
* **Python Libraries** - NumPy, Pandas, Matplotlib Scikit-Learn 
* **Web Technologies** - HTML, CSS, JavaScript, Flask 

## About the Dataset

* The dataset is from Kaggle.  It consists data regarding pricing of houses in one of the most expensive cities of India - Bengaluru. 
* It has 9 columns (area_type, availability, location, size, society, total_sqft, bath, balcony, price) and 13320 rows.
* There are numerical and categorical values.

## Data Preprocessing

* Drop uneccesary columns like 'society', 'availability', 'area_type' and 'balcony'.
* Handle missing values by dropping rows with missing values. 
* Some values in **total_sqft** are in the form of a range and some are float values. Wrote a function to convert the ranges into average value of range.  
* Performed feature engineering on the **size** column, and extracted number of bedrooms as a new feature called **BHK**.
* Created a new feature called **price_per_sqft** from the columns **total_sqft** and **price**.
* There were **1298** unique values in the **location** column. Performed *dimensionality reduction* and reduced the no. of columns to **241**.
* Found some outliers like -
    - Explored the **price_per_sqft** column and notice that the *min* and *max* values are very extreme. To handle this, we remove rows with **price_per_sqft** that are beyond 1 standard deviation, grouping by **location**. 
    - Visulaized the **price** and **total_area** columns and notice that there are some houses with 2 BHK that cost more than 3 BHK. 
    - When exploring the **bath** column, we notice that there are some houses where number of baths is a lot more than the number of bedrooms, which is pretty unusual. 
* Dropped unecessary columns. 
* Perform One Hot Encoding on the **location** column.

## Building a Model 

* Peformed **Cross Validation** on a **Linear Regression** model using the pre-processed data and found that the accuracy is on an average above **84%**.
* Perfomed **Grid Search** using different Regression models like Linear Regression, Lasso and Decision Trees and found that **Linear Regression** model performed the best. 
