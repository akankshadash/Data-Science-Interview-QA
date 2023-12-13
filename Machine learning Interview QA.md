# Machine Learning Interview Questions & Answers

### Q1 -What are the Bias and Variance in a Machine Learning Model and explain the bias-variance trade-off?
Bias and variance are two fundamental sources of error in machine learning models. Understanding these concepts is crucial for assessing and improving model performance.

##### a)Bias:
It is the error introduced by approximating a real-world problem, which may be extremely complex, by a simplified model. It measures how far off our predictions are from the actual values.

Characteristics:
High bias indicates that the model is too simple and fails to capture the underlying patterns in the data.
Models with high bias are often oversimplified and tend to underfit the data.

Example:
A linear regression model applied to a non-linear dataset will likely have high bias.

##### b)Variance:
It is the amount by which our model's predictions would change if we trained it on a different dataset. It measures the model's sensitivity to the fluctuations in the training data.

Characteristics:
High variance indicates that the model is too complex and is capturing noise in the training data.
Models with high variance are often too flexible and tend to overfit the data.

Example:
A high-degree polynomial regression model applied to a small dataset may have high variance.

Bias-Variance Trade-off:
The bias-variance trade-off is a fundamental concept in machine learning, representing the balance between a model's ability to capture the underlying patterns in the data (low bias) and its sensitivity to noise and fluctuations (low variance). The goal is to find the optimal level of model complexity that minimizes both bias and variance, ultimately leading to better generalization performance on unseen data.

### Q2- what are different ways to handle missing or corrupted data in a dataset

##### Imputation:

Imputation involves filling in missing values with estimated or calculated values based on the available data.

Methods:

a. Mean, Median, or Mode Imputation: Replace missing values with the mean, median, or mode of the observed values in the variable.eg - mean imputation -df['column_name'].fillna(df['column_name'].mean(), inplace=True)

b. Linear Regression Imputation: Predict the missing values using a linear regression model based on other variables.

c. k-Nearest Neighbors (KNN) Imputation: Replace missing values with the average of k-nearest neighbors in the feature space. -df_filled = KNN(k=3).fit_transform(df)

##### Deletion:

Deletion involves removing instances (rows) or features (columns) with missing or corrupted data.

Methods:
a. Listwise Deletion (Row Deletion): Remove entire rows with missing values.-df.dropna(inplace=True))

b. Pairwise Deletion: Keep observations with valid values for specific analyses, ignoring missing values in other variables.

c. Feature Deletion: Remove entire columns if a significant portion of their values are missing.-df.dropna(axis=1, inplace=True)

Note:
Deletion can lead to a reduction in the size of the dataset, potentially losing valuable information.It is suitable when the missing data is small in proportion to the total dataset.

##### Data Augmentation:

Data augmentation involves generating new samples based on the existing data to replace or supplement missing or corrupted values.

Methods:

Interpolation: Estimate missing values by interpolating between existing values.Linear Interpolation- df['column_name'].interpolate(method='linear', inplace=True)

Extrapolation: Estimate missing values by extrapolating from existing values.

Data Synthesis: Generate synthetic data to replace or supplement missing values.SMOTE FOR SYNTHETIC DATA- df_synthetic, _ = SMOTE().fit_resample(df, df['target_column'])

Note:
Data augmentation is useful when missing data follows a pattern that can be reasonably estimated or simulated.
It requires careful consideration of the domain and the nature of the missing data.
