# xtream AI Challenge

# Introduction - Price of a diamond

In this tutorial I've tested different Machine Learning models to approach a linear regression problem concerning the price of a diamond.
The problem starts with a dataset that collects data from different diamond's features: *carat*, *cut*, *color*, *clarity*, *table*, *x*, *y*, *z* and *price*. Each of them hide an insight which I'd like to reveal by using different ML models and the main goal of the project is to make a regression of the price distribution.
After a simple data analysis where we are able to identify the relationships between each data, we start by feeding different model that are evaluated subsequently.

# ML regression

After dividing the dataset into *train* and *test* set, we remove the price from the starting dataframe since it's what we want to predict. I decided to choose three ML models: *Decision Tree Regressor*, *Random Forest Regressor* and *XGBoost Regressor*. We have evaluated their performances on the test set after training each model on the train set. Then, we called a method to reveal the importance of each feature in the regression and we can see that, surprisingly, the most important feature for 2 models is the *y* instead of the *carat* that is proportional to the *price*, as the correlation matrix shows us. The *Decision Tree* instead has revealed the *carat* feature as the most important one for the regression. For this reason I've decided to set-up a GridSearch to find the best parameters for the regression. Surprisingly, the performance reached by the tuned model is not sufficient as the one of the remained models. In the end, as we could think, *XGBoost* has obtained the best score.

---

## How to run
1. Download the repository by git clone [https://github.com/poporubeus/xtream-ai-assignment.git](https://github.com/poporubeus/xtream-ai-assignment.git)
2. Open files "Diamonds_assignment-Data_Analysis.ipynb" and "Diamonds_assignment-Prediction.ipynb".
