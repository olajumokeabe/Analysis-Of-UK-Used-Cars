## Analysis-Of-UK-Used-Cars

A pre-owned vehicle, also known as a used car or second hand car, is a vehicle that has been previously owned by one or more retail owners. 

![hypatia-h_3752fa0ea1ecc7009b18e6ee3e4992e8-h_e75109965c65ffd0ffb98e0367bf9ad5-300](https://github.com/olajumokeabe/Analysis-Of-UK-Used-Cars/assets/125363157/aa143a56-96dc-4032-bbdd-60b2ef960e6a)

# Introduction

These types of cars are available for purchase through various channels, such as franchise and independent car dealerships, rental car companies, buy here pay here dealerships, leasing offices, auctions, and private sale.


# Data Gathering

The objective of this analysis is to identify the factors that can help in determining the resale value of a pre-owned car in relation to the market, and to determine the optimal time for selling. In order to accomplish this goal, the following queries were posed:
•	What is the average price of each car manufacturer in the dataset?
•	What is the correlation between the price and mileage of the cars?
•	What is the distribution of fuel types across the dataset?
•	How does the road tax impact the price of the car?
•	What is the trend of the mileage and price of the cars over the years?
•	Which car manufacturer has the highest average price?
•	Is there a correlation between price and mileage?
•	What is the most common fuel type in the dataset?
•	How does the road tax impact the price of the car?
•	Is there a trend of increasing or decreasing price and mileage over the years?

# Data Collection and Transformation

The dataset was downloaded from Kaggle https://www.kaggle.com/datasets/adityadesai13/used-car-dataset-ford-and-mercedes and contained 13 files, which were 11 cleaned files and 2 unclean files.
The contents of uncleaned data also existed as clean data and so were deleted in order to avoid duplicates. The data were imported into Power Bi using the folder option and then transformed into Power query. Before the files were combined, the unwanted data properties were deleted.


![Screenshot (169)](https://github.com/olajumokeabe/Analysis-Of-UK-Used-Cars/assets/125363157/f2e4ca08-161b-416f-b999-c7601fdec7f2)

![Screenshot (166)](https://github.com/olajumokeabe/Analysis-Of-UK-Used-Cars/assets/125363157/bb73744d-9663-4956-a918-2b3d313a8638)


After combining data, the data types were checked and corrected appropriately as needed. It was then loaded into power bi for further analysis and visualization.

# Exploratory Data Analysis

The following are the actions I performed to answer the above business questions

![Screenshot (170)](https://github.com/olajumokeabe/Analysis-Of-UK-Used-Cars/assets/125363157/928fe90e-45e4-4792-8a8d-58a514dfc72f)

To calculate the age of the car I created an additional column with the DAX expression below:
Car Age = 2023 - 'Used Car Dataset'[Year]

In order to calculate price per mileage, rounded to two decimal points.
Price per Mileage = ROUND((DIVIDE('Used Car Dataset'[Price],'Used Car Dataset'[Mileage])),2)

Using the DAX function below I created a measure to calculate the average price per model 
Average Price per Model = CALCULATE(AVERAGE('Used Car Dataset'[Price]), 
                     FILTER(ALLSELECTED('Used Car Dataset'),'Used Car Dataset'[Model]=
                     MAX('Used Car Dataset'[Model]))
 
The image below is a representation of the visualization

 ![Used Car Report Image](https://github.com/olajumokeabe/Analysis-Of-UK-Used-Cars/assets/125363157/09ac71a4-2ecb-430b-a1e3-94ec3930a491)

 
  # INSIGHTS

The minimum age of UK used cars is 3 years

Across all 196 Model, Average Price per Model ranged from 1295 to 98,934.20. At 98,934.20, G Class had the highest Average Price per Model higher than Accent, which had the lowest Average Price per Model at 1295.

There's a significant correlation between price and mileage, we can say, mileage is an important determinant of the price paid for a pre owned car.
Petrol accounted for 55.16% Model of Cars, making it the highest fuel type. It can be assumed that petrol powered cars are produced more and are also relatively more affordable.

Total Price and Mileage diverged the most in the Year 2019, when Total Price were 504917430 higher than Mileage.
Across all Taxes Total Price ranged from 2876 to 944981805. The price of a car is not affected by the road tax, with exceptions to a one time event in which road tax affected the price of cars.

56.48% of all Models have Manual transmission, followed by Semi-Auto, Automatic, and Other. It also accounted for 40.83% of Total Price.

 # CONCLUSION
The major deteminants of the selling price of a used car are the model, period of usage, mileage, fuel type, however, it is also noteworthy to include the body condition of the vehicle and its engine .


Interact with the dashboard: www.novypro.com/project/analysis-of-uk-used-cars

Full guide of analysis:https://olajumokeajala.medium.com

Linkedin:www.linkedin.com/in/ganiyat-olajumoke-abe













