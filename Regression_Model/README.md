# Regression Model - Notes
This project focuses on building and evaluating regression models for predicting laptop prices based on various features. It involves data preprocessing, splitting the dataset, training different models, and evaluating their performance using RMSE (Root Mean Squared Error). Below is a summary of the key concepts and steps encountered throughout the project.
#mlzoomcamp

# Key Concepts:
1. Data Preprocessing
Column Normalization: Standardizing column names by making them lowercase and replacing spaces with underscores to make the dataset easier to work with.
Handling Missing Values: Learning two approaches for dealing with missing values: filling them with 0 or with the mean of the column (training data only).
Log Transformation: Applying a log transformation to the target variable (final_price) to stabilize variance and improve model performance, followed by reversing the transformation when interpreting results.
2. Train/Validation/Test Splitting
Using different random seeds to shuffle and split the dataset into training, validation, and test sets (with a 60%/20%/20% split).
Understanding how different random splits of the data can affect model performance and how to ensure reproducibility using random seeds.
Combining train and validation sets for final model training.
3. Model Training
Linear Regression: Training simple linear regression models without regularization and exploring the limitations of matrix inversion errors (e.g., singular matrices).
Ridge Regression (L2 Regularization): Adding a regularization parameter to the linear regression model to prevent overfitting and improve model stability.
Decision Trees and Random Forests: Exploring more complex models like Decision Trees and Random Forests to handle non-linear relationships in the data and reduce sensitivity to different data splits.
4. Model Evaluation
Root Mean Squared Error (RMSE): Using RMSE as the primary metric to evaluate model performance. RMSE measures the average error between predicted and actual values, and lower values indicate better model performance.
Standard Deviation of RMSE: Analyzing the consistency of model performance across different random seeds by calculating the standard deviation of RMSE scores. A low standard deviation implies stable model performance.
5. Key Takeaways
Model Stability: Through multiple experiments with different random seeds and models, you observed that some models, such as Random Forests, are highly stable (with a standard deviation of RMSE close to 0.0).
Regularization: The importance of using regularization (e.g., Ridge regression) to avoid issues like overfitting and numerical instability (such as singular matrix errors in linear regression).
Importance of Preprocessing: Handling missing values, applying transformations, and feature scaling (like standardization) all play a critical role in ensuring good model performance.
# Steps Involved
### Data Preprocessing:

Normalized column names and selected relevant features (ram, storage, screen, final_price).
Handled missing values using both 0-fill and mean-fill strategies.
Explored log transformation for the target variable.

### Train/Validation/Test Splitting:

Split the dataset with a 60%/20%/20% distribution, shuffling the data with various random seeds.
Combined train and validation sets for final model training.

### Model Training and Evaluation:

Trained linear regression models without regularization and Ridge regression models with varying values of the regularization parameter r.
Experimented with tree-based models like Decision Trees and Random Forests to improve model performance.
Evaluated models using RMSE on the test set, ensuring to reverse any log transformations when calculating final errors.

### Analysis of Results:
Calculated RMSE and its standard deviation across different seeds to evaluate model stability.
Compared RMSE values with provided options to determine the best model.
