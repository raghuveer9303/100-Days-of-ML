## Day 2: Building a Preprocessing Pipeline

On Day 2, we delved deeper into data preprocessing by constructing a robust pipeline for handling both numerical and categorical features. Using the Titanic dataset, we performed comprehensive preprocessing steps that can be reused and extended for any machine learning project. The tasks included:

- Imputation of missing values
- Scaling numerical features
- Encoding categorical variables
- Combining transformations using a column transformer
- Visualizing the processed data

These steps emphasize modularity and scalability, laying a strong foundation for machine learning pipelines.

---

### Key Concepts:

1. **Pipeline Construction**:
   - **Pipelines** automate preprocessing steps, ensuring consistency and reducing the likelihood of human error. They are particularly useful for applying transformations to training and testing datasets without leakage of information.
   - **Resources**:
     - [Scikit-learn Pipeline Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.pipeline.Pipeline.html)

2. **Handling Missing Values**:
   - **Numerical Features**: Missing values in numerical features (e.g., `Age`, `Fare`) were imputed using the median.
   - **Categorical Features**: Missing values in categorical features (e.g., `Embarked`, `Sex`) were replaced with the most frequent category.
   - **Resources**:
     - [Scikit-learn SimpleImputer Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.impute.SimpleImputer.html)

3. **Feature Scaling**:
   - **Min-Max Scaling** was applied to numerical features, scaling their values to a range of [0, 1]. This is critical for models that are sensitive to feature magnitudes.
   - **Resources**:
     - [Scikit-learn MinMaxScaler Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.MinMaxScaler.html)

4. **Categorical Encoding**:
   - **One-Hot Encoding** was used to convert categorical variables into binary columns, ensuring the machine learning models can process them effectively.
   - **Resources**:
     - [Scikit-learn OneHotEncoder Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.OneHotEncoder.html)

5. **Column Transformer**:
   - A **ColumnTransformer** was employed to combine separate pipelines for numerical and categorical features into a single preprocessing step.
   - **Resources**:
     - [Scikit-learn ColumnTransformer Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.compose.ColumnTransformer.html)

---

### Steps in the Pipeline:

1. **Numerical Preprocessing**:
   - Imputed missing values with the median.
   - Scaled features using Min-Max scaling.

2. **Categorical Preprocessing**:
   - Imputed missing values with the most frequent value.
   - Encoded categories into binary format using one-hot encoding.

3. **Combining Preprocessing Steps**:
   - Unified the transformations using a `ColumnTransformer` for streamlined processing of both numerical and categorical features.

4. **Feature Consolidation**:
   - Transformed data was merged into a single dataset, ready for machine learning models.

---

### Visualizing Preprocessed Data:

1. **Histograms**:
   - Visualized distributions of numerical features post-scaling to assess uniformity.

2. **Correlation Heatmap**:
   - Evaluated relationships between numerical features using a correlation matrix, highlighting potential collinearity.

---

### Train-Test Split:
- Preprocessed data was split into training and testing sets using an 80-20 ratio.
- Ensures the model is trained on one set of data and evaluated on another to avoid overfitting.

---

### Next Steps:
- Use the preprocessed data to train machine learning models.
- Experiment with feature selection and hyperparameter optimization to improve model performance.
- Explore advanced techniques such as custom transformers and feature engineering.

---
