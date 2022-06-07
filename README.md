# Laptop Prices Predictor
1) Designed a web app that predicts the price of the laptop given the configurations.

2) Scraped the laptops data from flipkart.com using python and BeautifulSoup package

3) Developed Linear, Lasso, and Random Forest Regressors using GridsearchCV to get the best model.


# Links and Resources Used
1) PyCaret Library: https://pycaret.org/
2) Streamlit Library: https://www.streamlit.io/
3) Packages: pandas, numpy, sklearn, flask, streamlit, joblib
4) Model Deployment Github: https://github.com/krishnaik06/Dockers


# Web Scraping
This is the Flipkart website comprising of different laptops. This page contains the specifications of 24 laptops. So now looking at this, we try to extract the different features of the laptops such as:
1) Description
2) Processor
3) RAM
4) Storage
5) Display
6) Warranty
7) Price

So we extract the data from 7 pages so our dataset now consists of the information the 168 different laptops.
Link to my article: https://towardsdatascience.com/learn-web-scraping-in-15-minutes-27e5ebb1c28e


# Feature Engineering
We go through all the features one by one and keep adding new features. I have made the following changes and created new variables: RAM - Made columns for Ram Capacity in GB and the DDR version
Processor - Made columns for Name of the Processor, Type of the Processor, Generation
Operating System - Parsed the Operating System from this column and made a new column
Storage - Made new columns for the type of Disk Drive and the capacity of the Disk Drive
Display - Made new columns for the size of the laptop(in inches) and touchscreen
Description - Made new columns for the company and graphic card


# Data Preprocessing
There are a few columns which are categorical here but they actually contain numerical values.So we need to convert few categorical columns to numerical columns. These are DDR_Version,Generation,Storage_GB,Price.


# Exploratory Data Analysis
![processor_type](https://user-images.githubusercontent.com/102171965/172411487-1a418442-f5f1-4922-bae9-9857acfc05db.png)

![diskdrive](https://user-images.githubusercontent.com/102171965/172411725-91c67213-fde8-46af-a8b9-63276c89c5a4.png)

![RAM_GB](https://user-images.githubusercontent.com/102171965/172412014-ce2f50e9-86aa-4955-8692-3a81a5da4e00.png)


# Model Building
Traditional Method
Used scikit-learn library for the Machine Learning tasks. Applied label encoding and converted the categorical variables into numerical ones.Then I splited the data into training and test sets with a test size of 20%. I tried three different models ( Linear Regression, Random Forest Regression, XGBoost) and evaluated them using Mean Absolute Error.
