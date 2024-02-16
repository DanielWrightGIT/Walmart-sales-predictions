# 🏬 Walmart Sales Predictions using Prophet 🏬
## Table of Contents
1. [Project Overview](#project-overview)
2. [Data](#data)
3. [Methodology](#Methodology)
4. [EDA](#EDA)
5. [Modification of Data](#modification-of-data)
6. [Visualization](#visualization)
7. [Discussion of Results](#Discussion-of-Results)


### Project Overview
The purpose of this project is to use Prophet, a forcasting tool created by Meta to predict future weekly sales for the Walmart corporation. It is important to note that while these are futures predictions Walmart has only released historical data publicly meaning that the predicted events have already come to pass. The parameters of this model extend for 2 years past the end point of the dataset and conclude in the year 2015.


### Data
The origins of the data are from the Walmart corporation and were uploaded to Kaggle.com by user "Mikhail" on 02/13/2024.
https://www.kaggle.com/datasets/mikhail1681/walmart-sales

### Methodology
- Python: EDA, modification, and modeling


### EDA
Inspection of the data shows that there are no duplicates, NA values or other abnormalities present in the dataset. This is to be expected from a large corporation such as Walmart with high quality standards in data maintenance.

### Modification of Data
- Irrelevant Columns Dropped: Store, Holiday Flag, Temperature, Fuel Price, CPI, Unemployment
- Renaming Columns: Prophet requires the name of the date column to be "ds" and the price column to be "y" for fitting the model.
- Cap: Modeling also requires an established cap. The cap was determined by looking at the greatest sales numbers and rounding up to the next million.
- Reformatting Date: Initially the dataset's date format was dd-mm-yyyy. Prophet requires the data to be in the yyyy-mm-dd format so the values were reformatted for modeling. 


### Visualization
*figure 1* Shows the predicted future sales for walmart contrasted with past sales from the years 2010 - late 2012
![forecast](https://github.com/DanielWrightGIT/Walmart-sales-predictions/assets/158070869/c703a44c-629d-4ef7-a6e9-4a10ff27b402)

*figure 2* Shows the sales associated with specific months
![yearly trend](https://github.com/DanielWrightGIT/Walmart-sales-predictions/assets/158070869/fcfcc527-2c7c-438b-96f8-ae9785e05676)


### Discussion of Results
  The figures clearly show that Holiday time is optimal for generating sales at Walmart. Before December in Novemner and October you can see the average individual saving up their money to unload it around the holidays. You can also clearly notice a severe dip in sales after the holidays resulting in a collective loss of profit. 
  The majority of December sales are towards the middle and end of the month. Pre-holiday slump could potentially be prevented by offering discounts on popular goods around Fall to lure in thrifty spenders. Greater focus does not need to be applied in December as there will always be a significant proportion of spenders who wait until the last minute to purchase gifts. It is unlikely that the post-holiday sump can be prevented but could potentially be alleviated through increased discounts on popular products. 
