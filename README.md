# Problem Statement and Project Description
Retail Sales Prediction is a regression machine learning project. Rossmann operates over 3,000 drug stores in 7 European countries. Currently, Rossmann store managers are tasked with predicting their daily sales for up to six weeks in advance. Store sales are influenced by many factors, including promotions, competition, school and state holidays, seasonality, and locality. With thousands of individual managers predicting sales based on their unique circumstances, the accuracy of results can be quite varied. You are provided with historical sales data for 1,115 Rossmann stores. The task is to forecast the "Sales" column for the test set. Note that some stores in the dataset were temporarily closed for refurbishment.

Businesses use sales forecasts to determine what revenue they will be generating in a particular timespan to empower themselves with powerful and strategic business plans. Important decisions such as budgets, hiring, incentives, goals, acquisitions and various other growth plans are affected by the revenue the company is going to make in the coming months and for these plans to be as effective as they are planned to be it is important for these forecasts to also be as good.

The work here forecasts the sales of the various Rossmann stores across Europe for the recent six weeks and compares the results from the models developed with the actual sales values.

# Project Files Description
This project contains two executable file, a technical document and a presentation as follows:

**Executable Files:**
* **ML Regression Sales Prediction for Rossman project.ipynb** - Google Collab notebook containing data summary, exploration, visualisations and modeling.
* **ML Regression Sales Prediction for Rossman project Part 2.ipynb** - Google Collab notebook containg model hyperparameter tuning, model performance, evaluation and conclusion.

#### <u>Data fields</u>
#### Most of the fields are self-explanatory.

* **Id** - an Id that represents a (Store, Date) duple within the set
*  **Store** - a unique Id for each store
*  **Sales** - the turnover for any given day (Dependent Variable)
* **Customers** - the number of customers on a given day
* **Open** - an indicator for whether the store was open: 0 = closed, 1 = open
* **StateHoliday** - indicates a state holiday. Normally all stores, with few exceptions, are closed on state holidays. Note that all schools are closed on public holidays and weekends. a = public holiday, b = Easter holiday, c = Christmas, 0 = None
* **SchoolHoliday** - indicates if the (Store, Date) was affected by the closure of public schools
* **StoreType** - differentiates between 4 different store models: a, b, c, d
* **Assortment** - describes an assortment level: a = basic, b = extra, c = extended. An assortment strategy in retailing involves the number and type of products that stores display for purchase by consumers.
* **CompetitionDistance** - distance in meters to the nearest competitor store
* **CompetitionOpenSince**[Month/Year] - gives the approximate year and month of the time the nearest competitor was opened
* **Promo** - indicates whether a store is running a promo on that day
* **Promo2** - Promo2 is a continuing and consecutive promotion for some stores: 0 = store is not participating, 1 = store is participating
* **Promo2Since**[Year/Week] - describes the year and calendar week when the store started participating in Promo2
* **PromoInterval** - describes the consecutive intervals Promo2 is started, naming the months the promotion is started anew. E.g. "Feb,May,Aug,Nov" means each round starts in February, May, August, November of any given year for that store

**Source Directory:**
* **Data & Resources.zip** - Includes sales data and store data for various Rossmann stores.

# Random Forest

Random forest is a supervised learning algorithm. It creates a "forest" out of an ensemble of decision trees, which are commonly trained using the "bagging" method. The bagging method's basic premise is that combining different learning models improves the overall output. Simply said, random forest combines many decision trees to produce a more accurate and stable prediction.

![image](https://github.com/humayel1/Sales-Prediction-for-major-chain-store-Rossman/assets/134964717/e5b8bfda-411a-4ca4-880c-a5ba8a5fc781)


Furthermore, the random forest classifier is efficient, can handle a large number of input variables, and provides correct predictions in most cases. It's a very strong tool that doesn't require any coding to implement.

# Exploratory Data Analysis

There were more sales on Monday, probably because shops generally remain closed on Sundays which had the lowest sales in a week. Store type B though being few in number had the highest sales average. The reasons include all three kinds of assortments specially assortment level b which is only available at type b stores and being open on sundays as well. The outliers in the dataset showed justifiable behaviour. The outliers were either of store type b or had promotion going on which increased sales.

![image](https://github.com/humayel1/Sales-Prediction-for-major-chain-store-Rossman/assets/134964717/0060e8b0-957e-43b1-886d-04af5b890c07)


![image](https://github.com/humayel1/Sales-Prediction-for-major-chain-store-Rossman/assets/134964717/a04e1122-13c6-4d62-b8f2-ad7af1e1dc83)


This is a count plot of open shops according to the day of the week. It's clear that the number of shops open on Sundays were very less and hence low sales. Some shops were closed on weekdays as well accounting to the stores closed due to refurbishment or holidays.
![image](https://github.com/humayel1/Sales-Prediction-for-major-chain-store-Rossman/assets/134964717/6876cafa-1553-4a7b-9a89-e1947f423579)


The above bar plot shows that the store types a, c and d have only assortment level a and c. On the other hand the store type b has all the three kinds of assortment strategies, a reason why average sales were high for store type b stores.
![image](https://github.com/humayel1/Sales-Prediction-for-major-chain-store-Rossman/assets/134964717/f6d90150-7aac-4b07-8a9b-032ef9a05db5)


Sales rise up by the end of the year before the holidays. Sales for 2014 went down there for a couple months - July to September, indicating stores closed due to refurbishment.
![image](https://github.com/humayel1/Sales-Prediction-for-major-chain-store-Rossman/assets/134964717/b45e9c56-0ec1-4d5a-96c2-bd003776dc04)

Store type B was open on all seven days of the week and had more sales than any other store type and promotion had a positive effect across all store types.

![image](https://github.com/humayel1/Sales-Prediction-for-major-chain-store-Rossman/assets/134964717/868c04a5-2060-4d02-b383-b74f6bcf2cea)

# Results
Random Forest Tuned Model gave the best results and the patterns that could be captured by the model without overfitting was captured achieving a R^2 of 0.95 which helps in allocation of resources and proper planning for the company's growth.
![image](https://github.com/humayel1/Sales-Prediction-for-major-chain-store-Rossman/assets/134964717/d1684c75-d5ed-447e-b114-fae297bd7e45)

# Model Performance and Evaluation

![image](https://github.com/humayel1/Sales-Prediction-for-major-chain-store-Rossman/assets/134964717/995bda6e-0a9c-4e85-9d78-ec7f2b89109d)


![image](https://github.com/humayel1/Sales-Prediction-for-major-chain-store-Rossman/assets/134964717/c1f13a8b-5c25-4bde-90b4-ba53f880e7fb)

## Store wise Sales Predictions

![image](https://github.com/humayel1/Sales-Prediction-for-major-chain-store-Rossman/assets/134964717/66114208-620f-45e1-b464-9b01f5128eec)

