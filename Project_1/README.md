>>Heart Disease Project — Heart.ipynb<<

The notebook currently has 53 cells and follows this pipeline:

1. EDA — Completed ✅
We have:

Imported NumPy, Pandas, Seaborn, Matplotlib
Loaded insurance.csv
Viewed the dataset using head()
Checked dataset shape
Checked data types and information
Generated descriptive statistics
Checked missing values
Plotted distributions for:
Age
BMI
Children
Charges
Analyzed categorical variables:
Sex
Smoker
Children
Created boxplots to inspect outliers
Created a correlation heatmap

So your Exploratory Data Analysis is done.

2. Data Cleaning & Preprocessing — Completed ✅
We:

Created a cleaned copy of the dataset
Removed duplicate rows
Checked missing values
Checked data types
Converted:
male/female → 0/1
no/yes smoker → 0/1
Renamed:
sex → is_female
smoker → is_smoker
Applied one-hot encoding to region
Converted the resulting data to integer format

3. Feature Engineering — Completed ✅
We created a new BMI category feature:

Underweight
Normal
Overweight
Obese

Then you converted those categories into dummy variables.

You also applied StandardScaler to:

age
bmi
children

This is a good step because you're preparing numerical features for a linear regression model.

4. Feature Selection / Statistical Analysis — Completed ✅
This is actually a strong part of your notebook.

We performed:

Pearson Correlation

Checked relationships between numerical/features and charges.

Chi-Square Test

Tested categorical features against binned insurance charges.
Used significance level α = 0.05.
Used the results to decide which features should be retained/dropped.

Then you selected your final features:

age
is_female
bmi
children
is_smoker
region_southeast
bmi_category_Obese
region_northwest

with:

charges

as the target.

5. Train-Test Split — Completed ✅
We have:

80% training data
20% testing data
random_state=42

So the dataset is properly divided into training and testing sets.

6. Machine Learning Model — Completed ✅
We trained:

Linear Regression

model = LinearRegression()
model.fit(X_train, y_train)

Then generated predictions:

y_pred = model.predict(X_test)

7. Model Evaluation — Partially Completed ⚠️
We have already calculated:

R² Score
Adjusted R²

This is good, but your ML evaluation is not complete yet.
You should still add:

MAE
MSE
RMSE
Actual vs Predicted plot
Residual/error analysis
Predicted vs Actual visualization
Comparison with other regression models
