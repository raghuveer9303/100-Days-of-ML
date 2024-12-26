# Day 5: Linear Regression - Boston Housing Prices

In this project, we implement a **Linear Regression** model to predict housing prices based on the number of rooms in a house using the **Boston Housing dataset**. Linear regression is a powerful statistical method used for modeling the relationship between a dependent variable and one or more independent variables.

Linear regression is a fundamental method used in supervised machine learning and statistical analysis to model the relationship between a dependent variable and one or more independent variables. In this case, we are using it to predict **house prices** based on the **number of rooms** in a property.

We use the **Boston Housing dataset**, which contains data on various attributes of homes in the Boston area. The goal is to predict the median value of homes (MEDV) based on the average number of rooms per dwelling (RM).

## Key Concepts

### [Linear Regression](https://scikit-learn.org/stable/modules/linear_model.html#linear-regression)

Linear regression models the relationship between two variables by fitting a linear equation to observed data. The basic formula for a simple linear regression is:

\[
y = \beta_0 + \beta_1 \cdot x
\]

Where:
- \( y \) is the dependent variable (house price),
- \( \beta_0 \) is the intercept,
- \( \beta_1 \) is the coefficient of the independent variable (number of rooms),
- \( x \) is the independent variable (number of rooms).

The objective is to find the best-fit line that minimizes the sum of squared residuals, which is the difference between the actual and predicted values.

### [Training a Model](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LinearRegression.html)

Training a model involves feeding the data into the algorithm and allowing it to learn the relationship between the input variables (features) and the target variable. In this case, we train a linear regression model using the training data where the **independent variable** is the number of rooms (RM) and the **dependent variable** is the median home price (MEDV).

After training, the model learns the coefficients (\( \beta_0 \) and \( \beta_1 \)) that define the regression line.

### [Model Evaluation](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.mean_squared_error.html)

After training the model, we evaluate its performance using various metrics, such as:
- **Mean Squared Error (MSE)**: This is the average of the squared differences between the actual values and the predicted values. A lower MSE indicates better performance.
- **R-squared (R²)**: This metric explains the proportion of variance in the target variable (house prices) that is explained by the model. R² values close to 1 indicate a good fit, while values closer to 0 indicate a poor fit.

### [Residual Analysis](https://en.wikipedia.org/wiki/Residual_sum_of_squares)

Residuals are the differences between the observed (actual) values and the predicted values from the model. Plotting residuals helps to evaluate the quality of the model. There are two primary types of residuals analysis:
- **Histogram of residuals**: Helps identify if the residuals are normally distributed.
- **Residuals vs Predicted values plot**: Checks if there are any patterns in the residuals, which may indicate that the model is not correctly capturing the relationship between the variables.

The goal is for residuals to be randomly scattered without any obvious pattern. This indicates that the model has captured all of the linear relationships.

## Summary of Insights

1. **Model Fit**: The linear regression model showed a reasonable fit to the data, as evidenced by the **R-squared** value and the **residuals plot**.
2. **Prediction Accuracy**: The model’s predictions can be evaluated using **Mean Squared Error (MSE)** and **R-squared** metrics, where we observe that a higher R² value and lower MSE indicate better predictive performance.
3. **Model Assumptions**: The residual analysis suggests whether the linear regression assumptions hold, such as linearity, homoscedasticity (constant variance of residuals), and independence of residuals.

## Next Steps

1. **Feature Engineering**: Consider adding more features (e.g., crime rate, average distance to employment centers, etc.) to improve the predictive power of the model.
2. **Model Improvement**: Explore other regression techniques like **Ridge Regression** or **Lasso Regression** for regularization to improve performance on more complex datasets.
3. **Cross-validation**: Implement cross-validation to better assess the model’s performance and reduce overfitting.
4. **Visualization**: Further visualize model predictions with different features to better understand how the model behaves across the entire dataset.

---

For more information on linear regression and model evaluation, refer to the official documentation:

- [Scikit-learn Linear Regression](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LinearRegression.html)
- [Scikit-learn Model Evaluation](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.mean_squared_error.html)
- [Residuals in Regression](https://en.wikipedia.org/wiki/Residual_sum_of_squares)
