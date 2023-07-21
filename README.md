# Flight Fare Prediction using Linear Regression
This project aims to develop a machine learning model for EasyMyTrip, an online tour and travel website, to predict flight prices for Indian aviation companies, maximizing profit through optimized pricing strategies and addressing key research questions.

# Problem Statement
EasyMyTrip, a leading online tour and travel website, aims to maximize its profit by developing a machine learning model to predict flight prices for various Indian aviation companies. The business problem at hand is to address the research questions and leverage data analysis to optimize pricing strategies and revenue generation for EasyMyTrip.

Key considerations for this business problem include:

* Pricing Variations Across Airlines: EasyMyTrip seeks to understand if ticket prices vary significantly among different airlines. By analyzing historical data and incorporating airline-specific factors, the company aims to identify pricing patterns and determine how prices differ across airlines. This analysis will help EasyMyTrip tailor its pricing strategy to remain competitive and attract customers.

* Impact of Last-Minute Bookings: EasyMyTrip wants to examine how ticket prices change when they are purchased just 1 or 2 days before departure. By analyzing historical data and considering factors such as seat availability and demand fluctuations, the company aims to understand the price dynamics for last-minute bookings. This analysis will assist EasyMyTrip in optimizing pricing strategies for such scenarios and potentially capturing additional revenue.

* Correlation between Price and Departure/Arrival Times: EasyMyTrip aims to investigate whether there is a correlation between ticket prices and departure/arrival times. By analyzing historical data and considering factors such as peak travel periods, flight demand, and convenience preferences of customers, the company aims to uncover any trends or patterns in price variations based on specific departure or arrival times. This analysis will help EasyMyTrip optimize pricing strategies and provide customers with attractive options based on their preferred travel times.

* Price Variation based on Source and Destination Cities: EasyMyTrip wants to understand how ticket prices change based on the source and destination cities. By analyzing historical data and considering factors such as distance, popularity of routes, and competition, the company aims to identify pricing patterns for different city pairs. This analysis will help EasyMyTrip offer competitive prices on specific routes and adjust pricing strategies accordingly.

* Variation in Ticket Prices between Economy and Business Class: EasyMyTrip intends to explore the variation in ticket prices between Economy and Business class. By analyzing historical data and considering factors such as comfort, amenities, and customer preferences, the company aims to determine the price differentials between the two classes. This analysis will assist EasyMyTrip in setting optimal prices for each class and catering to the diverse needs of its customers.

By addressing these research questions and leveraging data analysis, EasyMyTrip aims to develop a machine learning model that accurately predicts flight prices. This model will enable the company to optimize pricing strategies, attract customers with competitive prices, and ultimately maximize its profit in the competitive online tour and travel industry.


# Research Questions

The aim of our study is to answer the below research questions:

a) Does price vary with Airlines?

b) How is the price affected when tickets are bought in just 1 or 2 days before departure?

c) Does ticket price change based on the departure time and arrival time?

d) How the price changes with change in Source and Destination?

e) How does the ticket price vary between Economy and Business class?

# Research Report:-

### A) Does price vary with Airlines?

There is significant variation in ticket prices among different airlines, with Air India and Vistara having the highest average prices, while AirAsia and Indigo have comparatively lower average prices. This suggests that airline choice plays a crucial role in determining ticket prices for customers.

### B) How is the price affected when tickets are bought in just 1 or 2 days before departure?

Price of tickets increases significantly when they are bought just 1 or 2 days before departure. This suggests that last-minute bookings tend to be more expensive, indicating a potential price premium for the convenience of booking close to the departure date.

### C) Does ticket price change based on the departure time and arrival time?

Ticket prices show variations based on the departure time and arrival time. Evening and night departures tend to have higher average prices, while late night departures and early morning arrivals have relatively lower average prices. This suggests that departure and arrival times can impact ticket pricing, potentially reflecting demand patterns and preferences of travelers.

### D) How the price changes with change in Source and Destination?

Flight prices vary depending on the source and destination cities. The prices range from the lowest for the Delhi-Hyderabad route (17,243.94) to the highest for the Chennai-Bangalore route (25,081.85). This suggests that different routes may have different pricing dynamics influenced by factors such as distance, demand, and competition among airlines.

### E) How does the ticket price vary between Economy and Business class?

The average price for Business class is significantly higher than that of Economy class, indicating a notable price variation between the two classes.

# Model Building Report

In model building process, I experimented with various regression algorithms and discovered that Random Forest, Gradient Boosting, and XGBoost performed well. After evaluating their performance, I chose Random Forest as it demonstrated good performance on both the train and test data, indicating that it is more generalized compared to the other algorithms.

Next, I proceeded with hyperparameter tuning to optimize the Random Forest model. However, the results of the hyperparameter tuning did not outperform the Random Forest model with its default parameters. Therefore, I decided to stick with the Random Forest model using its simple parameters.

To further assess the model's performance, I conducted cross-validation. As a result, the mean squared error (MSE) decreased, indicating improved model performance.

Finally, I evaluated the Random Forest model with simple parameters on both the train and test data to ensure its effectiveness and generalization.

## Model Summary

* Train and Test Set

|Data|	MSE|	RMSE|	MAE|	R-squared	|Adjusted R-squared|
|------|--------|--------|-----------|------------------|---------|
|	Train|	1,306,991	|1,143.245|	438.78|	0.99747|	0.99747|
|	Test|	5,568,1120|	7,461.98|	4,861.69	|0.89209|	0.89206|


* Validation Data

|Metric|	Mean|
|--------|------|
|Mean Squared Error (MSE)|	8,013,316|
|Root Mean Squared Error (RMSE)|	2,830.57|
|	Mean Absolute Error (MAE)|	1,166.64|
|	R-squared|	0.9845076|

## Top predictors
Below are the top variables that have the most significant impact on whether it will rain tomorrow or not.

|Variables	|Importance|
|---------|-------------|
|class_Economy	|0.881975|
|duration|	0.052071|
|days_left|	0.020889|

Airlines prices are primarily dependent on these factors, with 95% of the variation in prices being attributed to them. Specifically, 88% of the variation in prices can be explained by the factor of one class_economy alone.
