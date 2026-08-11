Ford Car Price Prediction — What you have done

1. Dataset Loading & Basic Analysis ✅

You loaded the Ford car dataset and performed:

head()
Dataset shape
info()
describe()
Missing-value check
Column inspection

Your target variable is:

price

2. Exploratory Data Analysis (EDA) ✅
We created several visualizations:

Price distribution histogram
Correlation heatmap
Year vs Price boxplot
Mileage vs Price scatter plot
Engine Size vs Price boxplot
Transmission vs Price boxplot
Fuel Type vs Price boxplot
Model vs Price boxplot

So your EDA is quite good and mostly complete.

3. Feature & Target Separation ✅
We separated:

X = df.drop(columns=['price'])
y = df['price']

So:

X → car features
y → car price

4. Categorical Encoding ✅
We used One-Hot Encoding for:

model
transmission
fuelType

using:

pd.get_dummies(..., drop_first=True)

You also experimented with Label Encoding using LabelEncoder.

So you have explored two encoding approaches.

5. Feature Scaling ✅
We used StandardScaler for numerical features:

year
mileage
tax
mpg
engineSize

This prepares the features for regression.

6. Train/Test Split ✅
We used:

Training → 67%
Testing → 33%
random_state = 42

7. Linear Regression Model ✅
We trained:

Linear Regression

on the one-hot encoded dataset.

Then you generated:

y_pred = model.predict(X_test)

So prediction is completed.

8. Model Evaluation — Partially Done ⚠️
We calculated:

R² Score ✅
Adjusted R² ✅

You also imported:

mean_absolute_error
mean_squared_error

but you didn't actually calculate MAE/MSE/RMSE yet.

9. Second Linear Regression Experiment ⚠️
We then trained another Linear Regression model using your Xlable dataset.

So you have essentially experimented with:

Model 1

One-Hot Encoding → Scaling → Linear Regression

Model 2

Label Encoding → Scaling → Linear Regression

You calculated R² for the second model as well.
