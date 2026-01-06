# Study of Models – Week 1 & Week 2

This repository contains **Week 1 and Week 2 assignments** for the *Study of Models* project. These assignments helped me understand the **basics of data science, statistics, data visualization, NumPy, Pandas, and machine learning models**.

All the work is done using **Python and Jupyter Notebooks**, and I have added comments in the code to explain what each step is doing.

---

## Folder Structure

```
WIDS_Week1/
│── WIDS_WEEK1_Study_of_models_Week1.ipynb
│── dataset/
│   └── CSV files used for Week 1 problems

WIDS_Week2/
│── WIDS_STUDY_OF_MODELS_WEEK2.ipynb
│── RIDGE_AND_LASSO.ipynb
│── housing.csv
```

---

## Week 1: Study of Models – Basics

### Theory Questions (Q1–Q5)

These questions focus on understanding basic concepts like:

* Difference between **supervised and unsupervised learning**
* Difference between **NumPy arrays, Pandas Series, and DataFrames**
* Why we use **box plots, histograms, scatter plots, and violin plots**
* Tracing **recursive functions** without running the code
* Basics of **hypothesis testing** and when to use t, F, and chi-square distributions

These questions helped in building strong theoretical understanding.

---

### Coding Questions (Q6–Q9)

All coding questions are implemented in:

`WIDS_WEEK1_Study_of_models_Week1.ipynb`

---

### Q6: Space Farm Productivity Crisis

**Dataset:** `farm_metrics.csv`

In this problem, we analyze data from a space farm.

What is done:

* Load the dataset using Pandas
* Find **mean, median, and variance** of plant height
* Find **correlation** between nutrient level and yield
* Generate fake yield values using **normal distribution** in NumPy
* Perform **matrix transpose and inverse** operations
* Plot:

  * Scatter plot of nutrient level vs yield
  * Histogram of simulated yields

---

### Q7: Lost Treasure Ship Analysis

**Dataset:** `sonar_points.csv`

This problem works with 3D sonar data.

What is done:

* Read coordinates using Pandas
* Calculate **distance from origin** using NumPy
* Normalize data so that mean = 0 and variance = 1
* Compute **covariance matrix**
* Plot:

  * Scatter plot of x vs y
  * Histogram of depth (z)
* Find **top 5 deepest points** using Pandas

---

### Q8: Chocolate Factory Quality Control

**Dataset:** `choco_quality.csv`

This problem analyzes quality of chocolate bars.

What is done:

* Remove missing values
* Use `.describe()` to see statistics
* Calculate a **quality score** using NumPy
* Add random noise using normal distribution
* Plot:

  * Scatter plot of cocoa % vs sugar %
  * Histogram of chocolate weight

---

### Q9: Interstellar Signal Analysis

This question focuses on NumPy matrix operations.

What is done:

* Generate random numbers between 0 and 2π
* Create **4×6 sine and cosine matrices**
* Compute:

  * Dot product of matrices (using transpose if needed)
  * Row-wise cross product of matrices

---

### Q10: Brain Round

This section includes logic-based questions like:

* Finding the poisoned wine bottle using logical thinking
* Understanding Spiderman train problem using probability and timing

These questions help improve reasoning skills.

---

## Week 2: California Housing Price Analysis

All Week 2 work is done in:

`WIDS_STUDY_OF_MODELS_WEEK2.ipynb`

**Dataset:** California Housing dataset (`housing.csv`)

---

### Dataset Description

The dataset contains information about houses such as:

* Location (latitude, longitude)
* Number of rooms and bedrooms
* Population and households
* Median income
* Median house value (target variable)

---

### Data Exploration

Steps performed:

* Checked dataset shape and column names
* Displayed first 10 rows
* Used `.info()` and `.describe()` to understand data
* Identified the feature with highest variance

---

### Univariate Analysis

* Plotted histograms for all numeric columns
* Tried different bin sizes
* Explained common ways to reduce skewness such as:

  * Log transformation
  * Square root transformation

---

### Outlier Detection

* Used box plots to find outliers in:

  * Median Income
  * Average Rooms
  * Population

---

### Correlation Analysis

* Computed correlation matrix
* Plotted heatmap
* Used correlation results to decide which features to keep

---

### Location-Based Visualization

* Scatter plot of Longitude vs Latitude
* Color shows Median House Value
* Point size shows Population

---

### PCA (Principal Component Analysis)

* Explained why **scaling is needed before PCA**
* Applied PCA on scaled data
* Plotted explained variance ratio
* Selected top 2 principal components
* Scatter plot of PC1 vs PC2 colored by house value

---

### Multiple Linear Regression

* Built a regression model using scikit-learn Pipeline
* Removed latitude and longitude from final model
* Printed coefficients and intercept

---

### Model Evaluation

Metrics used:

* Mean Squared Error (MSE)
* Mean Absolute Error (MAE)
* R² Score
* Adjusted R² Score

Also understood:

* Why high R² is not always good
* Why low training loss is not always preferred

---

### Model Plots

* Predicted vs Actual values
* Residuals vs Predicted values

---

## Bonus: Ridge and Lasso Regression

Implemented in:

`RIDGE_AND_LASSO.ipynb`

This notebook includes:

* Ridge regression (L2 regularization)
* Lasso regression (L1 regularization)
* Comparison with normal linear regression
* Explanation of overfitting and regularization

---

These assignments helped me understand:

* How to work with real datasets
* How to visualize and analyze data
* How regression models work
* How to evaluate model performance
