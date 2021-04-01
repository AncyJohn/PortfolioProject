# PortfolioProject: Salary prediction

Introduction:- This project is the development of a model that predicts the target feature 'salary' using 8 predictive features. This is the first project that I have done completely in python language. The project is done in the 4D framework: Define, Discover, Develop and Deploy.

Define:- The train and test data consists of the index column and 7 feature columns that can be used for the prediction process. This is a regression problem. We are to develop a machine learning model using the train data features that can be used to predict the salary of a set of completely unseen data.

Discover:- In this stage, we explore the structure and shape of the data. We also attempt to see if there any null/duplicate/wrong values. We discover the distribution of the target variable and the correlation between the variables.

The dataframe consists of both categorical numerical datatypes. First we look for any wrong data(in a logical sense) in the numerical columns by checking for any values below '0'. The minimum column values are 0 for the numerical features. Distribution of the response variable is found to be normal. This distribution plot also reveals the mean, quantiles and extreme values of the target. The box plot visualization reveals the presense of the outliers.
![image](https://user-images.githubusercontent.com/56666609/113226995-01807680-92ee-11eb-8eed-1ec15e266b04.png)

Now it is time to join the features and response dataframes. We use indexing to join the data and check for any duplicate values. There were 186 duplicate records that are dropped as part of the wrangling process. 
As part of the data preprocessing to train the data, categorical features are to be encoded into numerical features. The correlation between the variables are plotted on a heatmap.
![image](https://user-images.githubusercontent.com/56666609/113232822-68a42800-92fa-11eb-8efa-223a3627cd45.png)

Development:- Here, we develop a baseline model. We need to identify the most suitable machine learning algorithm for this specific problem. Starting from the simple linear regression model we chose to increase the complexicty of the model until we reach a certain threshold. I chose xgboost algorithm that gave a decent mse value. 

Feature engineering is an important stage to improve the efficiency of the algorithm. New column is added from the existing features. Hyper parameter tuning with grid search is used to find the best model. The final mse score is 355.38.

Feature importance with xgboost after training the model is plotted. The new feature column added is an important predictor for the model.
![image](https://user-images.githubusercontent.com/56666609/113234290-78713b80-92fd-11eb-8a7d-57de20fc389f.png)


Deploy:- The successful model is used for model prediction on the test features data and saved the predicted salaries as 'test_salaries' csv file.
