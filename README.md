# LGD-Forecasting

## Aim
The aim of this project is to forecast the Loss Given Default of the particular firm based on various internal and external factors.

## Variance inflation factor:
We have used VIF Variance Inflation Factor to assess the severity of multicollinearity in our
model. Multicollinearity occurs when independent variables in a regression model are highly
correlated with each other, which can lead to issues such as inflated standard errors and difficulties
in interpreting the individual coefficients of the variables. A VIF of 1 indicates no multicollinearity
whereas a VIF exceeding 5 or 10 is considered indicative of multicollinearity, suggesting that the
variance of the coefficient estimate for that variable is inflated by a factor of 5 or 10, respectively.
We used 2 different models for data modeling as shown in the figure above. We first ran Model 1
on our entire data. Once we got the results from Model 1, we then put our Model 1 results into
Model 2. Our model 2 only uses data of the members who have paid back at least some amount to the firm.

## 1. Logistic Regression
Logistic Regression is a statistical algorithm utilized for binary classification tasks,
aiming to model the relationship between a set of input variables and the probability of a
binary outcome. By fitting a logistic function to the data, this algorithm estimates the
probabilities of different classes and makes predictions based on a predefined threshold.
Its popularity stems from its simplicity, interpretability, and ability to handle numerical
and categorical input features effectively. In our analysis, we applied logistic regression
to the resampled training set. We then conducted cross-validated predictions on the
training set and assessed the model's performance using sensitivity, specificity &
accuracy. In our case, our Target Variable is $ Amount of Recovery and hence the
model predicts whether the firm is going to recover from the defaulted members or not.
(Yes/No)

## 3. Linear Regression
Linear regression is a statistical model used to analyze the
relationship between a dependent variable and one or more independent variables. It
assumes a linear relationship between the dependent variable (also called the response or
outcome variable) and the independent variables (also called predictors or features). The
goal of linear regression is to find the best-fitting linear relationship that minimizes the
difference between the observed values of the dependent variable and the values
predicted by the model. Like logistic regression, we performed cross-validated
predictions on the training set and evaluated the model's performance using MSE (Mean
squared error) & R-squared. Our outcome is $ amount of Recovery and LGD%.
