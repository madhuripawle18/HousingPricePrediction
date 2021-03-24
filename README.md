# Housing Price Prediction

![Website.png](https://github.com/madhuripawle18/HousingPricePrediction/blob/main/Website.png)

## Data Preprocessing

* Drop uneccesary columns like 'society', 'availability', 'area_type' and 'balcony'.
* Handle missing values by dropping rows with missing values. 
* Some values in total_sqft are in the form of a range and some are float values. Wrote a function to convert the ranges into average value of range.  
* Performed feature engineering on the size column, and extracted number of bedrooms as a new feature called BHK.
* Created a new feature called price_per_sqft from the columns total_sqft and price.
* There were 1298 unique values in the location column. Performed dimensionality reduction and reduced the no. of columns to 241.
* We explore the **price_per_sqft** column and notice that the *min* and *max* values are very extreme. So, there is a possibility that they are outliers. To handle this, we remove rows with price_per_sqft that are beyond 1 standard deviation, grouping by location. 
* Found some outliers like -
    - Visulaized the price and total_area columns and notice that there are some houses with 2 BHK that cost more than 3 BHK. 
    - When exploring the **bath** column, we notice that there are some houses where number of baths is a lot more than the number of bedrooms, which is pretty unusual. 
* Dropped unecessary columns. 
* Perform One Hot Encoding on the location column.

