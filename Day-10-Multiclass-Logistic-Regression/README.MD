# Day-9: Multi-class Logistic Regression

This session delves into advanced applications of Logistic Regression, including multiclass classification (One-vs-Rest and Multinomial approaches), dimensionality reduction for visualization, real-world application with the MNIST dataset, and advanced feature engineering with polynomial features.

---

## Key Concepts

### 1. **Logistic Regression Variants**
   - **One-vs-Rest (OvR)**: Fits separate binary classifiers for each class.
   - **Multinomial Logistic Regression**: Directly models all classes in a single optimization.

### 2. **Dimensionality Reduction**
   - **PCA (Principal Component Analysis)**: Reduces data to two dimensions for visualization while retaining maximum variance.

### 3. **Real-World Application**
   - Applying multinomial logistic regression to the MNIST dataset for handwritten digit classification.

### 4. **Feature Engineering**
   - **Polynomial Features**: Expands feature space to capture complex relationships by creating interaction terms and higher-order features.

---

## Documentation Links

- [Logistic Regression (Scikit-learn)](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html)
- [Train-Test Split](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.train_test_split.html)
- [StandardScaler](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.StandardScaler.html)
- [PCA (Scikit-learn)](https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.PCA.html)
- [Polynomial Features](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.PolynomialFeatures.html)
- [MNIST Dataset](https://scikit-learn.org/stable/auto_examples/classification/plot_digits_classification.html)

---

## Insights

1. **Logistic Regression Approaches**:
   - OvR is easier to interpret but can be less efficient compared to Multinomial Regression.
   - Multinomial regression provides better overall accuracy when directly modeling multiclass problems.

2. **Dimensionality Reduction**:
   - PCA is an effective tool for visualizing decision boundaries in multiclass classification.
   - It simplifies high-dimensional data for better interpretability.

3. **Real-World Application (MNIST)**:
   - Logistic regression performs well for medium-sized datasets but might struggle with highly complex patterns compared to more advanced models like Neural Networks.

4. **Feature Engineering with Polynomial Features**:
   - Expanding feature space using polynomial transformations improves the model's ability to capture non-linear relationships.

---

## Next Steps

1. **Explore Hyperparameter Tuning**:
   - Adjust the `C` parameter (inverse regularization strength) to analyze the trade-off between bias and variance.
   - Experiment with solvers like `saga` for larger datasets.

2. **Compare Models**:
   - Use other multiclass algorithms like Random Forest or Neural Networks for the MNIST dataset and compare performance metrics.

3. **Scaling to Larger Datasets**:
   - Implement logistic regression with stochastic optimization methods (e.g., SGDClassifier).

4. **Evaluate Polynomial Features**:
   - Assess if higher-degree polynomial transformations improve classification accuracy, keeping overfitting in check.

5. **Advanced Visualization**:
   - Apply t-SNE or UMAP for better visualization of high-dimensional data.

---

## References

- [Introduction to Logistic Regression](https://scikit-learn.org/stable/modules/linear_model.html#logistic-regression)
- [Iris Dataset Overview](https://archive.ics.uci.edu/ml/datasets/iris)
- [Multinomial Logistic Regression on MNIST](https://scikit-learn.org/stable/auto_examples/classification/plot_digits_classification.html)
- [Feature Engineering Guide](https://machinelearningmastery.com/feature-engineering/)

