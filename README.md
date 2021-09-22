# How can Real Estate Investors make better house price predictions in King County,Washington(USA)
Machine Learning Algorithm output using **Python** can be used to help investors to understand the mid-value housing market of the King County so as to invest in future.

## Introduction
In recent years, houses in King county has increased in leaps and bounds. According to [this Zillow Home Value Index](https://www.zillow.com/king-county-wa/home-values/), from 2020 to 2021, prices has increased by a whopping 19%. This has become a lucrative market for real estate investors to buy a property. Real Estate investors tend to buy houses, renovate them and then sell for higher price. 
A machine learning algorithm on historical data will help the business to understand the market well. It can address various questions  such as:
1. What can be the price of a new house in King County?
2. Which areas in the King County are the most profitable to acquire a new property?
3. Is renovation important for a house?
4. Which factors influence if a real estate investor wants to renovate a property it has bought recently? etc

The real estate investors are looking answers for the mid-value houses typically priced below a million dollar, typically with 2-6 bedrooms. This is  because, these houses get sold or rented more quickly as there is always a market for them,  thus establishing a steady flow of revenue for the investors. Cost of renovation is also managable and so more quicker is the income generation. 

**King County**

![king county2](https://user-images.githubusercontent.com/49127037/134259655-d210df1c-ecf2-4b0f-a323-fea33a51ec92.png)


## Data Collection

The dataset is retrieved from Kaggle. It contains 20K+ house records with 18 features such as no. of bedrooms, area of of the living area, zipcodes to where the houses are,etc, and their sale price for King County. The houses are sold between May 2014 and May 2015. The machine learning model should be able to predict future house price in this county.

## Exploratory Data Analysis

Here in this [notebook]() I do basic exploratory data analysis on the dataset to get an understand of the data. *Python packages like matplotlib and seaborn are used*. Things I covered :
* Getting an understanding of the data 
* Checking missing values and treating them
* Trimming the dataset to mid-level houses categories
* Analysis of the features with respect to price of the house
* Visualization of the location of the house with respect to few features of the house and how then can derive better business decision for the investor

## Feature Engineering and Data Preprocessing

In this [notebook]() I have tried following things :
* Created few features with the help of existing features , so as to derive more information to feed into the model . I have also created few graphs for data visualization to see how this new features are defining the price of the house
* Created dummy variables for the categorical features. 
* A heatmap of the correlation between price and other features is produced to understand which features are highly correlated with price

## Training models and evaluation and hyperparameter- tuning
Built models and then evaluate them in this [notebook](). Steps I have done are :
* Dividing the data into two parts: training and validation. To find the model, I use the training set and finally test the model on unseen data, which is the validation set
* Creating a baseline model using the median of house price across the zipcode groups. Mean Absolute Error (MAE) is calculated as the evaluation metric which is the error. Other complex models will be tested against this baseline model MAE. 
* 4 complex models are run for this regression task and best out of the lot with the lowest MAE is chosen as the final model. I got Random Forest Regression model with the lowest MAE
* Hyperparameter tuning of the RandomForest model and finally testing on the unseen data
* Getting the feature importance of the model which shows, which features have contributed the most in the final model

## Findings

**1. Presence of a Waterfront** : Exploratory data analysis shows that average price of a house is significatly high when the house has a waterfront. This can be clearly seen in the next pic , that houses near waterbodies(blue dots) like Lake Washington and few others have price > $800K. This can be an important information to real estate investors when they buy or acquire a house by helping them to formulate the price of the house
![image](https://user-images.githubusercontent.com/49127037/134278694-c53d0275-f79e-42f3-b304-7d7c0d316af3.png)
![image](https://user-images.githubusercontent.com/49127037/134275956-df336e54-80fc-4926-9e4e-bce6116870d1.png)

**2. Condition of the house**: EDA also shows, better is the condition of the house, more is the average sale price. This can help the investors in planning their funds in bettering the condition of a house in terms of wear and tear. 
However, the price range of condition 3-5 is not so different, so investors can plan to spend money to better the condition of the house to atleast 3.
![image](https://user-images.githubusercontent.com/49127037/134279885-e506402a-20f7-4519-94cd-9ab668f97e65.png)

**3. Grade of the house** : The highest grade quality (9 and above) of houses are found near Bellevue and Redmond . Average and above average i.e, Grade 6 and above are found all over King County, which is great for the investors. 
Also,as we see on the next picture, that grade of a house do impact the house price, and so low grade means investors spending money out of their pocket

![image](https://user-images.githubusercontent.com/49127037/134280378-14772d32-0b03-438f-8125-1048a0bd5f9a.png)
![image](https://user-images.githubusercontent.com/49127037/134279592-71157b9b-f04d-4ca8-9d89-eac5de11c9c1.png)

**4. Renovation of a house** : Renovating a house can definitely bring revenue for an investor. Though the percentage of house being renovated with the current sample is less than 5% but investors can definitely use this information if they invest in a not-so-great- building 
![image](https://user-images.githubusercontent.com/49127037/134281387-39accbd2-9826-4c53-8cb7-f9a4aba33eea.png)

**5. Age of the building**: : As we see in the graph, the age of the building does not influence price. This can be because old buildings can be repaired, remodelled and  renovated,  and we have seen from above analysis that these kind of changes fetch higher sale price. This can be good news to the investor as they can always acquire an old house and then rely on beautifying the house. 
![image](https://user-images.githubusercontent.com/49127037/134281034-66b56673-437f-4015-848b-e1e2a4604814.png)

**6. House with a basement or not** : A house with a basement has higher average saleprice. To maximize revenue, Real Estate investors can plan to buy majority of houses with a basement. Also, close to 40% of the houses in the sample have house with basement, so investors have a good chance in aquiring more houses with a basement
![image](https://user-images.githubusercontent.com/49127037/134282096-a71edda8-1f89-42cb-ac69-7998fe30c9db.png)







 


