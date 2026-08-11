Insurance Charges Project — Insurance.ipynb

Your Insurance notebook has 53 cells, so it is considerably further along.

A. Dataset + EDA ✅
We loaded:

insurance.csv

Then performed:

head()
Shape
info()
describe()
Missing-value check

B. EDA Visualizations ✅
We analyzed:

Age distribution
BMI distribution
Children distribution
Charges distribution
Sex distribution
Smoker distribution

You also created:

Boxplots
Correlation heatmap

C. Data Cleaning ✅
We:

Created a cleaned dataset
Removed duplicates
Checked missing values
Checked data types

D. Encoding ✅
We converted:

male → 0
female → 1

no smoker → 0
yes smoker → 1

Then renamed them:

sex → is_female
smoker → is_smoker

You also encoded region.

E. Feature Engineering ✅
We created:

BMI Category

Underweight
Normal
Overweight
Obese

Then one-hot encoded the BMI categories.

F. Feature Scaling ✅
We applied StandardScaler to:

Age
BMI
Children

G. Statistical Feature Analysis ✅
This is an important part of your Insurance project.
We performed:

Pearson Correlation

to analyze numerical feature relationships.

You also performed:

Chi-Square Test

on categorical features against binned insurance charges.

You used:

α = 0.05

and used the results for feature selection.

H. Final Feature Selection ✅
We final dataset uses:

age
is_female
bmi
children
is_smoker
region_southeast
bmi_category_Obese
region_northwest

Target:

charges

I. Train/Test Split ✅
We used:

80% Training
20% Testing
random_state = 42

J. Machine Learning ✅
We trained:

Linear Regression
and generated:

y_pred

K. Model Evaluation — Partially Done ⚠️
We calculated:

R² Score ✅
Adjusted R² ✅
