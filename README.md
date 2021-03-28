# PortfolioProject: Salary prediction

Introduction:- This project is the development of a model that predicts the target feature salary using 8 predictive features. This is the first project that I have done completely in python language. The project is done in the 4D framework: Define, Discover, Develop and Deploy.

Define:- The train and test data consists of the index column and 7 feature columns that can be used for the prediction process. This is a regression problem. We are to develop a machine learning model using the train data features that can be used to predict the salary of a set of completely unseen data.

Discover:- In this stage, we explore the structure and shape of the data. We also attempt to see if there any null/duplicate values. We discover the distribution of the target variable and the correlation between the variables.

Development:- Here, we develop a baseline model. We need to identify the most suitable machine learning algorithm suitable for this specific problem. Starting from the simple linear regression model we chose to increase the complexicty of the model until we reach a certain threshold. I chose xgboost algorithm that gave a decent mse value. Feature engineering has done on to this model for the required target mse. The final mse score is 355.38.

Deploy:- The successful model is used for model prediction on the test features data and saved the predicted salaries are saved as 'test_salaries' csv file.
