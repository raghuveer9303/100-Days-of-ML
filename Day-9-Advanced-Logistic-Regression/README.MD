# Day 9: Advanced Logistic Regression

This project demonstrates advanced techniques in Logistic Regression using the Telco Customer Churn dataset. It focuses on data preprocessing, model training, evaluation, and hyperparameter tuning while addressing class imbalance and providing insights into logistic regression concepts.

---

## Key Concepts

1. **Logistic Regression**  
   Logistic Regression is a statistical model that uses the sigmoid function to model the probability of a binary outcome.  
   - [Logistic Regression Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html)

2. **Data Preprocessing**  
   Preprocessing steps are essential for preparing raw data for modeling:
   - Convert categorical features using One-Hot Encoding: [OneHotEncoder](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.OneHotEncoder.html)
   - Standardize numerical features: [StandardScaler](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.StandardScaler.html)
   - Handle missing values: [Pandas `fillna`](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.fillna.html)

3. **Class Imbalance**  
   Addressed using SMOTE (Synthetic Minority Oversampling Technique) to balance classes in the training dataset:
   - [SMOTE Documentation](https://imbalanced-learn.org/stable/references/generated/imblearn.over_sampling.SMOTE.html)

4. **Model Evaluation**  
   Key metrics used to assess the model’s performance:
   - **Confusion Matrix**: [Confusion Matrix Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.confusion_matrix.html)
   - **Classification Report**: [Classification Report Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.classification_report.html)
   - **ROC-AUC Curve**: [ROC-AUC Documentation](https://scikit-learn.org/stable/auto_examples/model_selection/plot_roc.html)
   - **Precision-Recall Curve**: [Precision-Recall Curve Documentation](https://scikit-learn.org/stable/auto_examples/model_selection/plot_precision_recall.html)

5. **Hyperparameter Tuning**  
   Explored the impact of varying regularization strengths (`C`) and class weights on model performance.

---

## Steps Overview

1. **Data Loading**  
   - Load Telco Churn dataset using [Pandas `read_csv`](https://pandas.pydata.org/docs/reference/api/pandas.read_csv.html).

2. **Data Preprocessing**  
   - Handle missing values for `TotalCharges`.  
   - Encode categorical variables with One-Hot Encoding.  
   - Standardize numerical features.  
   - Map `Churn` to binary values (Yes=1, No=0).

3. **Class Imbalance Handling**  
   - Oversample the minority class using SMOTE.

4. **Model Training**  
   - Train a Logistic Regression model with balanced class weights.  
   - Tune hyperparameters to improve performance.

5. **Model Evaluation**  
   - Visualize results using a confusion matrix, ROC-AUC curve, and precision-recall curve.

---

## Insights

- Logistic Regression is highly effective for binary classification problems but sensitive to class imbalance.
- SMOTE improves performance by oversampling the minority class, ensuring balanced training data.
- Regularization strength (`C`) significantly impacts model performance and generalization.
- Precision-recall and ROC-AUC curves provide insights into model effectiveness, especially for imbalanced datasets.

---

## Next Steps

1. **Feature Selection**: Experiment with feature importance to reduce dimensionality.  
2. **Alternative Models**: Compare Logistic Regression with other models like Decision Trees or Random Forests.  
3. **Grid Search for Hyperparameter Tuning**: Optimize model parameters for better performance.  
4. **Deploy Model**: Implement the model in a production pipeline.

---

## References

- [Scikit-learn User Guide](https://scikit-learn.org/stable/user_guide.html)  
- [Imbalanced-learn Documentation](https://imbalanced-learn.org/stable/)
- [Pandas Documentation](https://pandas.pydata.org/docs/)  
- [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)  
- [Seaborn Documentation](https://seaborn.pydata.org/)  
