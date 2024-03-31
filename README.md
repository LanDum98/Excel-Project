# 10 Malls Istanbul Excel Project

### Project Overview
This project's aim is to provide insight into sales performance of 10 malls in Istanbul over the course of 27 months worth of customer sales data.

### Data Sources:
Kaggle: Original dataset can be downloaded [here](https://www.kaggle.com/datasets/mehmettahiraslan/customer-shopping-dataset/data)

### Tools:
- Excel

### Data Preparation

What was performed on this dataset:
1. Downloading and exploring the raw data
2. Cleaning and removing of any duplicates
    - No duplicates were found 
3. Formatting dates
    - dd/mm/yyyy
4. Creating new columns for analysis
    - age_group
    - The shoes category was counted as the clothing category

### Exploratory Data Analysis

EDA involved exploring the sales data to answer key questions:

1. How are other malls performing compared to each other?
2. What was the most sold products in these malls?
3. Who is going to the malls and what are they buying?

### Data Analysis

- IFS to Create age Group column
``` Excel
=IFS([@age]<30,"Young Adult",[@age]<47,"Middle Age",[@age]<62,"Late Adult",[@age]<100, "Senior")
```
- SUMIFS to create "Mall_Perfmance" Sheet
- INDEX MATCH on "Mall_Performance" Sheet
``` Excel
=INDEX(Performance_Month[[Cevahir AVM]:[Zorlu Center]],MATCH(O6&O5,Performance_Month[Month]&Performance_Month[Year],0),MATCH(O4,Performance_Month[[#Headers],[Cevahir AVM]:[Zorlu Center]],0))
```
- Pivot Tables to create dashboard

### Findings/Results

1. The top performing malls are: "Mall of Istanbul","Kanyon",and "Metrocity". They are dominating all the other competition in the dataset.
2. The most sold product in the malls are clothing. All other categories are not performing nearly as well. 
3. Customers that are consuming the most are the middle aged adults and late aged adults.

### Recommdations

In order to improve the performance of these malls the customer's experience should be prioritized.
- More accessiblity to all customers especially people with disabilities.
- Niche products and stores that would be more popular within the senior and yound adult age groups. 
- Improve the variety and quality of food and drinks being sold.

### Limitations

Helpful data that was not available about these malls:
- Size and capacity of these malls
- Customer experience 
- Foot traffic
- Top and bottom performing stores and restaurants these inside malls

The Author claims this a synthetic dataset.

