# Day 6: Multiple Linear Regression - Boston Housing Prices

In this project, we explore **Multiple Linear Regression** and extend the analysis by introducing **Polynomial Regression** to capture non-linear relationships in the **Boston Housing dataset**. Multiple regression allows us to model the relationship between a dependent variable and multiple independent variables.

## Introduction

Multiple linear regression is an extension of simple linear regression where more than one independent variable is used to predict the dependent variable. This provides a more nuanced understanding of how multiple features contribute to the prediction.

For this analysis, we use the **Boston Housing dataset**, aiming to predict the **median home price (MEDV)** based on various features like the number of rooms, crime rate, and more. We also introduce **Polynomial Regression** to model non-linear relationships.

---

## Key Concepts

### [Multiple Linear Regression](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LinearRegression.html)

Multiple linear regression models the relationship between one dependent variable and two or more independent variables. The regression equation is:

\[
y = \beta_0 + \beta_1 x_1 + \beta_2 x_2 + \dots + \beta_n x_n
\]

Where:
- \( y \) is the dependent variable (house price),
- \( \beta_0 \) is the intercept,
- \( \beta_i \) are the coefficients for each independent variable \( x_i \),
- \( x_i \) are the independent variables.

### [Model Evaluation](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.r2_score.html)

We evaluate the model’s performance using:
- **R-squared (R²)**: Represents the proportion of variance in the dependent variable explained by the model. Higher values (closer to 1) indicate better fit.
- **Adjusted R-squared**: Adjusts R² to account for the number of predictors in the model, penalizing overfitting.

Formula for Adjusted R²:
\[
\text{Adjusted } R^2 = 1 - (1 - R^2) \frac{n - 1}{n - p - 1}
\]
Where \( n \) is the number of observations and \( p \) is the number of predictors.

### [Multicollinearity and Variance Inflation Factor (VIF)](https://www.statsmodels.org/stable/generated/statsmodels.stats.outliers_influence.variance_inflation_factor.html)

**Multicollinearity** occurs when independent variables are highly correlated, which can distort the regression coefficients. We detect multicollinearity using the **Variance Inflation Factor (VIF)**:
- A VIF > 5 or 10 indicates significant multicollinearity.

### [Polynomial Regression](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.PolynomialFeatures.html)

Polynomial regression is a type of regression that models the relationship between the dependent and independent variables as an nth-degree polynomial. This allows for capturing non-linear relationships. 

Polynomial features are created using:
\[
y = \beta_0 + \beta_1 x + \beta_2 x^2 + \dots + \beta_n x^n
\]

---

## Summary of Insights

1. **Multiple Linear Regression**: The model performed well in predicting median house prices using multiple features. Key features such as the average number of rooms (RM) and lower status of the population (LSTAT) significantly influenced predictions.
2. **Adjusted R² Improvement**: Using Adjusted R² instead of plain R² helped us evaluate model performance while accounting for the number of predictors, indicating the model's reliability.
3. **Multicollinearity Check**: VIF analysis identified potential multicollinearity among some features, which may affect the interpretability of regression coefficients.
4. **Polynomial Regression**: Introducing polynomial terms improved model fit by capturing non-linear relationships, as evidenced by higher R² and Adjusted R² scores.

---

## Next Steps

1. **Feature Engineering**: Consider transformations or interaction terms for variables showing multicollinearity.
2. **Regularization Techniques**: Explore methods like **Ridge Regression** or **Lasso Regression** to handle multicollinearity and improve model interpretability.
3. **Cross-validation**: Validate the models using cross-validation techniques to ensure consistent performance across different datasets.
4. **Further Polynomial Exploration**: Experiment with higher-degree polynomials to see if they capture more complex patterns, but balance against potential overfitting.
5. **Visualization Enhancements**: Enhance visualizations for clearer representation of actual vs predicted values and residuals for both linear and polynomial models.

---

For more information on the methods and tools used, refer to the following documentation:

- [Scikit-learn Linear Regression](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LinearRegression.html)
- [Scikit-learn Polynomial Features](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.PolynomialFeatures.html)
- [Scikit-learn R² Score](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.r2_score.html)
- [Variance Inflation Factor (VIF)](https://www.statsmodels.org/stable/generated/statsmodels.stats.outliers_influence.variance_inflation_factor.html)