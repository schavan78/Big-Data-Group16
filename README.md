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
There are four dataset provided by Walmart:
[Link for the dataset](https://www.kaggle.com/competitions/walmart-recruiting-store-sales-forecasting/data)

The dataset from Kaggle is used for this project. The dataset contains historical sales data from 45 stores located in different regions. Each store is further divided into departments. It has three different csv files features, stores and sales data.


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
* The goal is to forecast Walmart's weekly sales based on past year sales on a weekly basis.
* To investigate how additional factors may influence weekly sales.
* To evaluate the different machine learning models such as XGBoost and KNN.
* To optimize the manufacturing process and therefore to increase income while lowering costs.
* To understand customer demographics and analyze the weekly sales and observe trends in data.
* To bring valuable insights in pricing decisions on sales performance.

## Research Objective and Question
* What are the impacts of temperature, fuel prices and various store promotions on weekly sales of different Walmart stores for two years using various AWS services such as Sagemaker, Quicksight, S3?
