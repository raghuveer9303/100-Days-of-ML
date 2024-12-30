# Day 8: Logistic Regression and Regularization

Today’s focus is on **Logistic Regression**, a fundamental classification technique, and exploring the impact of **regularization methods** like **L1**, **L2**, and **ElasticNet**. We'll also visualize decision boundaries and understand the effect of regularization on model performance.

---

---

## Introduction

Logistic regression is a classification algorithm that predicts probabilities using the **sigmoid function**. It is widely used in binary classification tasks. Today’s exercise includes:
1. Generating and visualizing a **sample dataset**.
2. Implementing and training a **logistic regression model**.
3. Exploring **regularization techniques** (L1, L2, ElasticNet).
4. Visualizing decision boundaries and exploring model interpretability.

For detailed documentation, refer to:
- [Scikit-learn Logistic Regression](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html)
- [Scikit-learn Regularization](https://scikit-learn.org/stable/modules/linear_model.html#logistic-regression)
- [Seaborn Documentation](https://seaborn.pydata.org/)

---

## Key Concepts

### Logistic Regression

Logistic regression estimates the probability \( P(y=1|X) \) using the sigmoid function:
\[
\sigma(z) = \frac{1}{1 + e^{-z}}
\]
Where \( z = X\theta \). The output is a value between 0 and 1, making it ideal for binary classification.

Documentation:
- [Logistic Regression on Wikipedia](https://en.wikipedia.org/wiki/Logistic_regression)
- [Sigmoid Function](https://en.wikipedia.org/wiki/Sigmoid_function)

### Sigmoid Function

The sigmoid function maps any input \( z \) to a probability between 0 and 1. We plotted this function to understand its shape and properties, highlighting the decision boundary at \( z = 0 \) where \( \sigma(z) = 0.5 \).

### Decision Boundaries

Visualizing decision boundaries helps us understand how logistic regression separates the classes in a dataset. Using contour plots, we overlaid the model's predictions on the dataset's feature space.

---

## Regularization Techniques

Regularization in logistic regression helps prevent overfitting by penalizing large coefficients. It adds a penalty term to the cost function.

### L1 Regularization (Lasso)

- Adds an **absolute value of coefficients** penalty.
- Encourages sparsity by setting some coefficients to 0.
- Ideal for feature selection.

Documentation: [L1 Regularization](https://scikit-learn.org/stable/modules/linear_model.html#lasso)

### L2 Regularization (Ridge)

- Adds a **squared value of coefficients** penalty.
- Shrinks coefficients toward 0 without eliminating them.
- Helps reduce multicollinearity and overfitting.

Documentation: [L2 Regularization](https://scikit-learn.org/stable/modules/linear_model.html#ridge)

### ElasticNet Regularization

- Combines L1 and L2 penalties:
\[
\alpha \cdot \text{L1 penalty} + (1-\alpha) \cdot \text{L2 penalty}
\]
- Provides a balance between L1’s feature selection and L2’s coefficient shrinking.

Documentation: [ElasticNet Regularization](https://scikit-learn.org/stable/modules/linear_model.html#elasticnet)

---

## Exploratory Data Analysis (EDA)

EDA was performed by converting the dataset into a **DataFrame**. Key steps included:
1. **Correlation Heatmap**: Explored relationships between features and the target.
2. **Pair Plot**: Visualized feature distributions and their separability by class.

Documentation:
- [Pandas DataFrame](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.html)
- [Seaborn Correlation Heatmap](https://seaborn.pydata.org/generated/seaborn.heatmap.html)
- [Seaborn Pair Plot](https://seaborn.pydata.org/generated/seaborn.pairplot.html)

---

## Insights and Next Steps

### Insights

1. **Logistic Regression**: A powerful yet interpretable algorithm for binary classification.
2. **Regularization**:
    - **L1**: Performs feature selection by zeroing out coefficients.
    - **L2**: Shrinks coefficients, reducing overfitting.
    - **ElasticNet**: Combines the strengths of both L1 and L2 regularization.
3. **Visualization**:
    - Decision boundaries provide an intuitive understanding of model predictions.
    - Correlation heatmaps and pair plots reveal feature relationships and class separability.

### Next Steps

1. **Hyperparameter Tuning**:
    - Use grid search to fine-tune the regularization strength (\( C \)) and mixing parameter (\( \alpha \)).
    - [GridSearchCV Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.GridSearchCV.html)
2. **Expand Dataset**:
    - Explore larger datasets with more features.
    - [Datasets in Scikit-learn](https://scikit-learn.org/stable/datasets/index.html)
3. **Compare Models**:
    - Compare logistic regression with other classifiers like SVM or Random Forest.
    - [SVM Documentation](https://scikit-learn.org/stable/modules/svm.html)
    - [Random Forest Documentation](https://scikit-learn.org/stable/modules/ensemble.html#random-forests)
4. **Advanced Metrics**:
    - Evaluate models using precision, recall, F1-score, and AUC-ROC curves.
    - [Classification Metrics](https://scikit-learn.org/stable/modules/model_evaluation.html#classification-metrics)

By exploring regularization and visualization techniques, we’ve gained insights into how logistic regression performs on datasets and learned to mitigate overfitting using regularization.