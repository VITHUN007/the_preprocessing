# Retail Product Data Analysis
## Project Overview
This project focuses on  preprocessing, and analyzing the Retail Product Dataset with Missing Values to prepare the data for predictive modeling. The end result is a model-ready dataset.

The primary challenges addressed are the high percentage of missing values in key columns (Category, Price, Rating) and prepare a complete dataset with no missing values.

##  Dataset details

The initial dataset contains

- Category : it contains 2748 missing values around 63 % 
- Price : it contains around 174  missing values around 4% 
- Rating:it contains 2050 missing values  around 47%
- Stock :it contains 1352 missing values  around 31%
- discount:it contains 392 missing values around 9%

## Datapreprocesing

#### Imputation:

Numerical: Discount and Rating filled with Median. Price filled with Mean (creating a price column).

Categorical: Category and Stock missing values filled with the string 'Missing'.

####  Encoding:

One-Hot Encoding (OHE): Applied to Category and Stock, creating new binary columns (e.g., Category_Missing, Stock_In Stock) using pd.get_dummies(), which is the fastest way to perform One-Hot Encoding

#### Scaling:

Price: Scaled using StandardScaler, MinMaxScaler, and RobustScaler to create standardized features for modeling.

#### Visualization
Visualization: A Scatter Plot of Price vs. Rating was generated.



## Strageries used
- for stock,categories missing values i uesd "missing" used Ohe dummies here
- for  price missing values we used "mean" to find its values.
- for rating ,discount we used "median" here

- y median used not mean? 
 
 --  Median Imputation was chosen for Rating and Discount because it is robust to outliers. it provides a reliable central estimate for skewed numerical data --
 
 - used minmax,standard,robust scalar in "price"

 - used scatter to view price vs rating

 - done all changes mentioned above and created a new updated dataset as "processed_data.csv" 

## Dataset used
- Used this dataset from kaggle
 https://www.kaggle.com/datasets/himelsarder/retail-product-dataset-with-missing-values

## conclusion 
- we done a complete datset without missing value and ready for train modal and stored as a new file.now we can use this dataset since we removed all missing values using data cleaning and preprocessing