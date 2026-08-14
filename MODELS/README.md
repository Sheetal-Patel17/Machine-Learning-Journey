# 🚢 Titanic Survival Prediction — Classification Algorithms

This project explores different **Machine Learning classification algorithms** to predict whether a passenger survived the Titanic disaster.

The project focuses on understanding the complete machine-learning workflow, including **data preprocessing, feature encoding, train-test splitting, feature scaling, model training, prediction, and model evaluation**.

---

## 📌 Project Overview

The Titanic dataset contains information about passengers aboard the RMS Titanic, including features such as:

* Passenger class
* Sex
* Age
* Number of siblings/spouses aboard
* Number of parents/children aboard
* Fare
* Port of embarkation

The target variable is:

**`survived`**

* `0` → Did not survive
* `1` → Survived

The objective is to build classification models that can learn patterns from the passenger data and predict survival.

---

## 🧠 Algorithms Implemented

The following classification algorithms were implemented and evaluated:

1. **Logistic Regression**
2. **K-Nearest Neighbors (KNN)**
3. **Gaussian Naive Bayes**
4. **Decision Tree Classifier**
5. **Support Vector Machine (SVM)**

---

## 🔄 Machine Learning Workflow

The notebook follows these major steps:

### 1. Data Loading

The Titanic dataset is loaded using Seaborn:

```python
df = sns.load_dataset("titanic")
```

### 2. Data Cleaning

Unnecessary or redundant columns are removed, including:

* `class`
* `who`
* `adult_male`
* `deck`
* `embark_town`
* `alive`

Missing values in the `age` column are replaced with the mean age, while rows with missing `embarked` values are removed.

### 3. Feature Encoding

Categorical variables such as `sex` and `embarked` are converted into numerical values using `LabelEncoder`.

### 4. Feature and Target Separation

The dataset is divided into:

* **X** → Input features
* **y** → Target variable (`survived`)

### 5. Train-Test Split

The dataset is split into training and testing sets using an 80/20 ratio.

```python
train_test_split(
    X,
    y,
    test_size=0.2,
    random_state=42
)
```

### 6. Feature Scaling

Feature scaling is applied for algorithms that benefit from normalized feature ranges.

```python
from sklearn.preprocessing import StandardScaler

sc = StandardScaler()
X_train_sc = sc.fit_transform(X_train)
X_test_sc = sc.transform(X_test)
```

### 7. Model Training

Each classification algorithm is trained using the training dataset.

### 8. Model Evaluation

The models are evaluated using:

* Accuracy Score
* Confusion Matrix
* Classification Report
* Precision
* Recall
* F1-Score

---

## 📊 Models

### Logistic Regression

Logistic Regression is used as a baseline classification model for predicting passenger survival.

```python
from sklearn.linear_model import LogisticRegression

model = LogisticRegression()
model.fit(X_train, y_train)
```

---

### K-Nearest Neighbors

KNN classifies passengers based on the classes of their nearest data points.

```python
from sklearn.neighbors import KNeighborsClassifier

knn = KNeighborsClassifier(n_neighbors=5)
knn.fit(X_train_sc, y_train)
```

Feature scaling is applied before using KNN.

---

### Gaussian Naive Bayes

Gaussian Naive Bayes is a probabilistic classification algorithm based on Bayes' theorem.

```python
from sklearn.naive_bayes import GaussianNB

model_NB = GaussianNB()
model_NB.fit(X_train, y_train)
```

---

### Decision Tree

Decision Tree classification creates a tree-like structure of decisions to classify passengers.

```python
from sklearn.tree import DecisionTreeClassifier

model_DT = DecisionTreeClassifier(random_state=42)
model_DT.fit(X_train_sc, y_train)
```

---

### Support Vector Machine

SVM attempts to find an optimal decision boundary between the classes.

An **RBF kernel** is used in this project.

```python
from sklearn.svm import SVC

model_SVC = SVC(
    kernel='rbf',
    random_state=42
)

model_SVC.fit(X_train_sc, y_train)
```

---

## 📈 Evaluation Metrics

The models are evaluated using the following metrics:

### Accuracy

Measures the overall percentage of correctly classified observations.

### Precision

Measures how many of the passengers predicted as survivors actually survived.

### Recall

Measures how many of the actual survivors were correctly identified.

### F1-Score

The harmonic mean of precision and recall, providing a balanced measure of model performance.

### Confusion Matrix

Shows the number of:

* True Positives
* True Negatives
* False Positives
* False Negatives

---

## 🛠️ Technologies & Libraries

This project was developed using **Python** and Jupyter Notebook.

### Libraries Used

* **NumPy** — Numerical computations
* **Pandas** — Data manipulation and analysis
* **Seaborn** — Dataset loading and visualization
* **Matplotlib** — Data visualization
* **Scikit-learn** — Machine learning algorithms and evaluation

---

## 📁 Project Structure

```text
Titanic-Classification/
│
├── Classification_Algorithms_Titanic_Model.ipynb
└── README.md
```

---

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone <your-repository-url>
```

### 2. Navigate to the project directory

```bash
cd Titanic-Classification
```

### 3. Install the required libraries

```bash
pip install numpy pandas seaborn matplotlib scikit-learn
```

### 4. Open the notebook

```bash
jupyter notebook Classification_Algorithms_Titanic_Model.ipynb
```

Run the notebook cells sequentially to reproduce the analysis and model results.

---

## 🎯 Learning Objectives

Through this project, I explored:

* Data preprocessing
* Handling missing values
* Categorical feature encoding
* Train-test splitting
* Feature scaling
* Classification algorithms
* Model prediction
* Confusion matrices
* Classification reports
* Comparing different machine-learning approaches

---

## 🔮 Future Improvements

Possible improvements to this project include:

* Hyperparameter tuning using GridSearchCV or RandomizedSearchCV
* Cross-validation
* Feature engineering
* Comparing additional classification algorithms
* Creating a model-performance comparison table
* Visualizing confusion matrices
* ROC-AUC curve comparison
* Improving feature encoding techniques
* Deploying the best-performing model using Flask or Streamlit

---

## 👨‍💻 Author

SHEETAL PATEL

This project was created as part of my learning journey in **Machine Learning and Classification Algorithms**.
