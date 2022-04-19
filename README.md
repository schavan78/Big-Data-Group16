# Big-Data-Group16

This project is a part of the ITCS 6100 - Big Data Analytics for Competitive Advantage course from the University of North Carolina at Charlotte.

## Team Members
* Ankita Marathe
* Sanket Gaikwad
* Aniket Varade
* Sourabh Kumbhar
* Sandeep Chavan

## Communication plan
We plan to communicate 3 times per week through zoom or in-person meetings based on the availability of the group members. The meetings will last for 2-3 hrs each.
## Data Resource
There are four datasets provided by Walmart:
[Link for the dataset](https://www.kaggle.com/competitions/walmart-recruiting-store-sales-forecasting/data)

The dataset from Kaggle is used for this project. The dataset contains historical sales data from 45 stores located in different regions. Each store is further divided into departments. It has three different CSV files features, stores, and sales data.


|Column Name      | Description   |                                                                                        Type   |
|-----------------|-------------- |---------------------------------------------------------------------------------------------- |
|Store            | Numerical value indicating the store number                                                          |Integer |
|Dept             | The department number                                                                                |Integer|
|Date             |   Date indicating the week                                                                           | Date  | 
|Weekly_Sales|   Sales for the given department in the given store| Number|
|IsHoliday|  whether the week is a special holiday week |Boolean|
|Temperature| Average temperature in the region|Float|
|MarkDown| Anonymized data related to promotional markdowns that Walmart is running|Float|
## Business Problem or Opportunity, Domain Knowledge
* To forecast Walmart's weekly sales based on the past two years' sales on a weekly basis using AWS services (Sagemaker, Quicksight, and S3).
* To investigate how additional factors may influence weekly sales.
* To evaluate the different machine learning models as XGBoost and KNN.
* To optimize the manufacturing process and therefore increase income while lowering costs.
* To understand customer demographics and analyze the weekly sales and observe trends in data.
* To bring valuable insights into pricing decisions on sales performance.

## Research Objective and Question
* What are the impacts of temperature, fuel prices, and various store promotions on weekly sales of different Walmart stores for two years?

## Data Preparation
The following three csv files are included in the dataset:

train.csv is a spreadsheet with 421570 rows and 5 columns. The columns include data for a store, department, date, weekly sales, and whether or not a given week is a holiday week.

store.csv is a 45-row, three-column spreadsheet. The columns correspond to the types of stores, as well as their sizes.

This file, features.csv, has 8190 rows and 12 columns. This file contains additional information on the stores as well as the regions in which they are located. It contains statistics for the date, temperature, gasoline price, consumer price index, and unemployment rate for the region in which a specific store is located.

* ###  Merging the dataset 
We have to merge the datase into one dataframe. 
```
master_df = train_df.merge(stores_df, how='left').merge(features_df, how='left')
```
* ### Extracting Date Information
 The sales are given for Years 2012-2012 on weekly basis. So we have to split the date column to extract information for year, month and week.
```
def split_date(df):
    df['Date'] = pd.to_datetime(df['Date'])
    df['Year'] = df.Date.dt.year
    df['Month'] = df.Date.dt.month
    df['Day'] = df.Date.dt.day
    df['WeekOfYear'] = (df.Date.dt.isocalendar().week)*1.0   
    
split_date(master_df)
```
## Exploratory data analysis
<img src = "img/negative-weekly%20sales.png" width="700" height ="350">
<img src = "img/missing%20values%20markdown.png" width="700" height ="350">
<img src = "img/weekly%20sales%20with%20isholiday.png" width="700" height ="350">
<img src = "img/weekly%20sales.png" width="700" height ="250">
<img src = "img/yearly%20weekly%20sales.png" width="700" height ="350">
<img src = "img/Screen%20Shot%202022-04-19%20at%201.50.52%20PM.png" width="700" height ="350">


