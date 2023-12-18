# Data Visualize and Analysis
## 1: Observed the dataset's basic information and found the columns having missing values.
![missing data](picture/visualizing_missing_data.png)

- ehail_fee: the missing indexes equal to the datapoint of the dataset => remove ehail_fee
- Other columns that have missing values include: VendorID, store_and_fwd_flag, RatecodeID, passenger_count, payment_type, trip_type,congestion_surcharge and they have the same percentage of missing values

## 2: Preprocess
### Outliers:
![scatter plot between total_amount vs Continous variables](https://github.com/VOTUANANH01/Data-Visualize-and-Analysis/blob/main/picture/visualizing%20scatterplot%20total_amounts%20vs%20Continuous%20variable.png)

- fare_amount, total_amount, and extra columns have negative values that do not gain insight in EDA => remove the negative values.
- Trip_distance has the 0 value but scatters all along total_amount => keep it for analysis.
 
![boxplot between total_amount and categorical](https://github.com/VOTUANANH01/Data-Visualize-and-Analysis/blob/a33db0842764b444c24b8ce706e5664a202fce62/picture/visuaizing%20boxplot%20between%20total_amount%20vs%20Categorical%20variable.png)

- improvement_surcharge,mta_tax, congestion columns have negative values that do not gain insight in EDA => remove the negative values.
- RatecodeId,passenger_count, and mta_tax columns have some outliers, which are 99,0 and 3.55 => do more research => suggesting removing or replacing them with the most count values.

### NaN/missing values:
![countplot of missing values](https://github.com/VOTUANANH01/Data-Visualize-and-Analysis/blob/a33db0842764b444c24b8ce706e5664a202fce62/picture/visualizing%20countplots%20have%20missing%20data.png)

- VendorID = 2, store_and_fwd_flag = N, passenger_count = 1 and trip_type = 1  have the most count => replace missing values with the most count values.
- payment_type have values: 1 (credit card) and 2 (cash) with almost the same percentage => replace missing values with randomly between 1 and 2.

### Decode categorical variables
### merging two datasets: the current one with [taxi zone look up](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page)

### extract time _diff = (lpep_dropoff_datetime - lpep_pickup_datetime).seconds/60, pickup/dropoff month, weekday, hour and bin_hours into [3 bins](https://nyc.gov/site/tlc/passengers/taxi-fare.page): [16,20) - rush, [20,6) - overnight, [6,16) - other 

 ## 3: EDA Univariate:
### EDA continuous variables:
  ![](https://github.com/VOTUANANH01/Data-Visualize-and-Analysis/blob/a33db0842764b444c24b8ce706e5664a202fce62/picture/eda_continuous_variable.png)
### EDA caterigocal variables:
 ![](https://github.com/VOTUANANH01/Data-Visualize-and-Analysis/blob/a33db0842764b444c24b8ce706e5664a202fce62/picture/eda_categorical_variable.png)
#### EDA dual caterigocal variables:
![](https://github.com/VOTUANANH01/Data-Visualize-and-Analysis/blob/a33db0842764b444c24b8ce706e5664a202fce62/picture/eda_dual_categorical_variable.png)
![](https://github.com/VOTUANANH01/Data-Visualize-and-Analysis/blob/a33db0842764b444c24b8ce706e5664a202fce62/picture/Countplot%20of%20pickup_hour.png)
![](https://github.com/VOTUANANH01/Data-Visualize-and-Analysis/blob/a33db0842764b444c24b8ce706e5664a202fce62/picture/Countplot%20of%20dropoff_hour.png)

- As observed in the plot above, the dataset is highly unbalanced.
- Generally, there is no difference between pickup and drop off.


## 4: EDA Bivariate:
- The range values of tip_amount for EDA: [0,61.12]
- The range values of total_amount for EDA: [0, 80,38]

### EDA continuous variables with tip_amount:
![](https://github.com/VOTUANANH01/Data-Visualize-and-Analysis/blob/a33db0842764b444c24b8ce706e5664a202fce62/picture/eda_continuous_variable_with%20tip_amount%20.png)
- There are not many columns that have a linear relationship to tip_amount
### EDA categorical variables with tip_amount:
![](https://github.com/VOTUANANH01/Data-Visualize-and-Analysis/blob/a33db0842764b444c24b8ce706e5664a202fce62/picture/eda_categorical_variable_with_tip_amount%20.png)
#### EDA dual categorical variables with tip amount:
![](https://github.com/VOTUANANH01/Data-Visualize-and-Analysis/blob/a33db0842764b444c24b8ce706e5664a202fce62/picture/eda_dual_categorical_variable_with_tip_amount%20.png)
 - There are many overlaps on these boxplots, especially on time variables and outliers appear thickly and scatter through tip_amount.
### EDA categorical variables with total_amount:
![](https://github.com/VOTUANANH01/Data-Visualize-and-Analysis/blob/a33db0842764b444c24b8ce706e5664a202fce62/picture/eda_categorical_variable_with_total_amount%20.png)
- While other columns overlap, the boxplot RatecodeID shows that distribution values of 1 and 5 are lower than the others and some outliers. The lowest number of samples belongs to 6. On the other hand, 3 and 4 have the largest range of the number of samples and the total amount.
#### EDA dual categorical variables with total_amount:

![](https://github.com/VOTUANANH01/Data-Visualize-and-Analysis/blob/a33db0842764b444c24b8ce706e5664a202fce62/picture/eda_dual_categorical_variable_with_total_amount%20.png)

- In some boxplots between location variables and total_amount, we can see a slight difference between drop-off and pick-up on the distribution values. But on the time variables, there is no difference between pick-up and drop-off.
  
### comparison between Time variables and tip_amount, total_amount
![]() 
 
