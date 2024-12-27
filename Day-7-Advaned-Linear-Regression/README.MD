# Day 7: Advanced Linear Regression (Ridge and Lasso)

In this day, we explore **Advanced Linear Regression** techniques, particularly **Ridge** and **Lasso** regression. These techniques extend the basic linear regression model by incorporating regularization to prevent overfitting and improve model generalization.

## Key Concepts

### [Ridge Regression](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.Ridge.html)

Ridge regression is a form of linear regression that adds an **L2 penalty** to the loss function, encouraging smaller coefficients and reducing model complexity. This method does not remove features but shrinks the coefficients toward zero, reducing the influence of less important variables.

The cost function for Ridge regression is:

\[
J(\theta) = \sum_{i=1}^{m} (y_i - \hat{y}_i)^2 + \lambda \sum_{j=1}^{n} \theta_j^2
\]

Where:
- \( \lambda \) is the regularization parameter controlling the strength of the penalty,
- \( \theta_j \) are the coefficients of the model.

### [Lasso Regression](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.Lasso.html)

Lasso regression introduces an **L1 penalty** (sum of absolute values of coefficients). It has the ability to drive some coefficients exactly to zero, effectively performing feature selection. This helps in eliminating irrelevant features, making the model simpler and easier to interpret.

The cost function for Lasso regression is:

\[
J(\theta) = \sum_{i=1}^{m} (y_i - \hat{y}_i)^2 + \lambda \sum_{j=1}^{n} |\theta_j|
\]

Where:
- \( \lambda \) is the regularization parameter controlling the strength of the penalty.

### [Model Comparison](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LinearRegression.html)

We compared three types of regression models:
1. **Linear Regression**: The baseline model without any regularization.
2. **Ridge Regression**: Incorporates the L2 penalty to shrink coefficients.
3. **Lasso Regression**: Incorporates the L1 penalty and performs feature selection.

Metrics used to evaluate the models:
- **R-squared (R²)**: Represents how well the model explains the variance in the data.
- **Mean Squared Error (MSE)**: Measures the average squared difference between the predicted and actual values.

### [Regularization Paths](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.Ridge.html)

The regularization paths for Ridge and Lasso show how the coefficients change as the regularization parameter \( \lambda \) is varied. As \( \lambda \) increases:
- **Ridge** coefficients decrease but do not become zero, meaning all features remain in the model.
- **Lasso** coefficients shrink towards zero, with some coefficients becoming exactly zero, effectively eliminating less relevant features.

---

## Summary of Insights

1. **Linear Regression**: The standard linear regression model did not perform as well as regularized models, showing signs of overfitting when tested on unseen data.
2. **Ridge Regression**: This model showed improved generalization compared to the linear regression, as the L2 penalty helped shrink the coefficients.
3. **Lasso Regression**: Lasso's ability to shrink some coefficients to zero allowed for feature selection, leading to a more interpretable and sparse model.
4. **Model Comparison**: Ridge and Lasso outperform basic linear regression, with Lasso providing the added benefit of feature selection.

---

## Next Steps

1. **Hyperparameter Tuning**: Further explore the effect of the regularization parameter \( \lambda \) on model performance by conducting more detailed hyperparameter tuning.
2. **Non-linear Models**: Investigate non-linear regression techniques like polynomial regression or decision tree-based models to capture more complex relationships in the data.
3. **Cross-validation**: Use cross-validation techniques to ensure that the models are robust and generalize well to new data.

By understanding and implementing these advanced regression techniques, you can better handle complex datasets and improve the accuracy and interpretability of your predictive models.