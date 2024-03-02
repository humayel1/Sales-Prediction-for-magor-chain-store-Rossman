
<p align="center"> 
  
</p>
<h1 align="center">  Regression - Retail Sales Prediction: Predicting sales of a major store chain Rossmann
 </h1>
<h3 align="center"> AlmaBetter Verified Project - <a href="https://www.almabetter.com/"> AlmaBetter School </a> </h5>

<p align="center"> 
</p>
<h2> Problem Statement and Project Description</h2>

<p>In seven European nations, Rossmann runs more than 3,000 pharmacies. Store managers at Rossmann are currently required to forecast their daily sales up to six weeks ahead of time. Numerous factors, such as competition, school and state holidays, seasonality, locality, and promotions, affect store sales. The accuracy of the statistics can vary greatly since thousands of managers forecast sales based on their own set of conditions. Historical sales information for 1,115 Rossmann establishments is given to you. Predicting the "Sales" column for the test set is the task. It should be noted that a few of the dataset's stores were briefly closed for renovations.</p>

<p>Product interest continues to fluctuate from time to time. No company can focus on financial expansion without accurately determining the interest of its customers and the future demand for its products. The process of projecting demand or sales of a specific product over a given time period is known as sales forecasting. In this project, a machine learning model for sales forecasting will be developed and a real-world business problem will be solved.

Here, our objective is to project each store's sales for the next six weeks, identify the variables that affect it, and offer suggestions for raising the figures.

Approach
<li> Business Problem 
<li> Data Collection and Preprocessing <p>

<h2> :floppy_disk: Project Files Description</h2>

<p>This project contains two executable file, a technical document and a presentation as follows:</p>
<h4>Executable Files:</h4>
<ul>
  <li><b>Rossmann_Sales_Prediction_Vithika_Karan.ipynb</b> - Google Collab notebook containing data summary, exploration, visualisations and modeling.</li>
  <li><b>Rossmann_Sales_Prediction_Part_2_Vithika_Karan_ipynb.ipynb</b> - Google Collab notebook containg model hyperparameter tuning, model performance, evaluation and conclusion.</li>
</ul>


<h4>Source Directory:</h4>
<ul>
  <li><b>Data & Resources.zip</b> - Includes sales data and store data for various Rossmann stores.</li>
</ul>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2> :book: Random Forest</h2>

<p>Random forest is a supervised learning algorithm. It creates a "forest" out of an ensemble of decision trees, which are commonly trained using the "bagging" method. The bagging method's basic premise is that combining different learning models improves the overall output.
Simply said, random forest combines many decision trees to produce a more accurate and stable prediction.
</p>

<p>Furthermore, the random forest classifier is efficient, can handle a large number of input variables, and provides correct predictions in most cases. It's a very strong tool that doesn't require any coding to implement.</p>


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2> :chart_with_upwards_trend: Exploratory Data Analysis</h2>
<p>There were more sales on Monday, probably because shops generally remain closed on Sundays which had the lowest sales in a week. 
Store type B though being few in number had the highest sales average. The reasons include all three kinds of assortments specially assortment level b which is only available at type b stores and being open on sundays as well.
The outliers in the dataset showed justifiable behaviour. The outliers were either of store type b or had promotion going on which increased sales.</p>
<img src="image/DayOfWeek.png" alt="Sales Results" style="max-width:40%;"> <img src="image/storetypeb.png" alt="Sales Results" style="max-width:40%;">
<p>Store type B was open on all seven days of the week and had more sales than any other store type and promotion had a positive effect across all store types.<p>
<img src="image/salesb.png" alt="Sales Results" style="max-width:40%;"> <img src="image/promotion.png" alt="Sales Results" style="max-width:40%;">

<h2> :chart_with_upwards_trend: Results</h2>
<p>Random Forest Tuned Model gave the best results and the patterns that could be captured by the model without overfitting was captured achieving a R^2 of 0.95 which helps in allocation of resources and proper planning for the company's growth.
            <img src="image/result.png" alt="Sales Results" style="max-width:70%;"><p>


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)




![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)
