# pizza_price_predict
This notebook walks through the process of predicting pizza prices using machine learning. We start by cleaning and exploring a dataset, then train several models to predict pizza prices. The goal is to compare different models, see which one works best, and understand which factors influence pizza pricing.

Data Preprocessing:
- We load the pizza data and clean the price column by removing currency symbols and commas, and then convert the prices from Indonesian Rupiah (IDR) to USD.
- Since some of the data columns are categorical (like toppings, variants, etc.), we use label encoding to convert them into numerical values for the models.

Exploratory Data Analysis (EDA):
- We start by visualizing the price distribution to see how prices are spread across the dataset.
- We also take a look at the frequency of different pizza diameters, toppings, variants, and sizes using bar charts and count plots.
- Boxplots are used to explore the relationship between price and factors like toppings or size.

Model Training:
- We split the data into a training set and a test set.
- Then, we train five different regression models to predict pizza prices:
- Random Forest
- Support Vector Machine (SVM)
- Linear Regression
- Gradient Boosting
- XGBoost

Model Evaluation
- We evaluate each model’s performance using the R2 score, which shows how well the model is predicting the prices.
- A bar plot is used to compare the R2 scores of all five models to see which one performs the best.

We also look at which features are most important for predicting pizza prices. This is done by examining the feature importance values from the Random Forest, Gradient Boosting, and XGBoost models.
We use bar charts to visualize these feature importances.

After training the models, we save the best-performing one (Gradient Boosting) using joblib so we can use it later to predict prices on new data.
