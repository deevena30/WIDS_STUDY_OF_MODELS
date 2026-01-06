# Study of Models – Week 1 & Week 2

This repository contains **Week 1 and Week 2 assignments** for the *Study of Models* course. These assignments helped me understand the **basics of data science, statistics, data visualization, NumPy, Pandas, and machine learning models**.

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

This week focuses on **understanding the data, building a proper ML pipeline, training a model, and analyzing the results**.

All the work is done in:

`WIDS_STUDY_OF_MODELS_WEEK2.ipynb`

---

## 1. Data Explanation

**Dataset:** California Housing Dataset (`housing.csv`)

Each row represents a housing block in California.

Important columns:

* `longitude`, `latitude` → location of the block
* `housingMedianAge` → age of houses
* `totalRooms`, `totalBedrooms` → room information
* `population`, `households` → people living in the block
* `medianIncome` → income level of the area
* `medianHouseValue` → house price (this is the **target variable**)

The goal is to **predict median house value** using the other features.

---

## 2. Understanding the Data

Steps performed:

* Checked **shape of dataset** (rows and columns)
* Listed **column names**
* Displayed **first 10 rows** to understand structure
* Used `.info()` to check data types and missing values
* Used `.describe()` to understand mean, spread, and variance

From this, we identified which features have high variance and wide range of values.

---

## 3. Data Visualization & Analysis

### Histograms (Univariate Analysis)

* Plotted histograms for all numeric columns
* Tried different bin sizes
* Observed skewness in features like income and population

**Common ways to reduce skewness (explained in comments):**

* Log transformation
* Square root transformation
* Box-Cox method

---

### Box Plots (Outlier Detection)

* Used box plots to detect outliers in:

  * Median Income
  * Average Rooms
  * Population

This helps in understanding extreme values in the data.

---

### Correlation Analysis

* Computed correlation matrix
* Plotted heatmap
* Observed that **latitude and longitude have weak direct correlation** with house value

This was used as a reason to **exclude latitude and longitude** in the final regression model.

---

### Location-Based Visualization

* Scatter plot of Longitude vs Latitude
* Color represents Median House Value
* Point size represents Population

This plot helps visually understand how house prices vary across locations.

---

## 4. Machine Learning Pipeline

A **scikit-learn Pipeline** is used to make the workflow clean and structured.

Pipeline steps:

1. **Scaling** – StandardScaler is used so that all features are on the same scale
2. **Model** – Multiple Linear Regression is applied

**Why scaling is needed:**

* Features have very different ranges
* Scaling helps models and PCA work correctly

---

## 5. PCA (Dimensionality Reduction)

Steps:

* Applied PCA on scaled features
* Plotted explained variance ratio
* Selected top 2 principal components

**Why PCA is used:**

* To reduce dimensions
* To understand main patterns in the data

Scatter plot of PC1 vs PC2 is colored using Median House Value.

---

## 6. Model Training & Results

* Trained Multiple Linear Regression model
* Printed model **coefficients** and **intercept**

### Evaluation Metrics Used:

* Mean Squared Error (MSE)
* Mean Absolute Error (MAE)
* R² Score
* Adjusted R² Score

**Important observations:**

* High R² does not always mean a perfect model
* Very low training loss can indicate overfitting

---

## 7. Model Performance Plots

* **Predicted vs Actual plot** → shows how close predictions are to real values
* **Residuals vs Predicted plot** → helps check patterns and errors

These plots are useful to judge model quality.

---

## Bonus: Ridge & Lasso Regression

Implemented in:
`RIDGE_AND_LASSO.ipynb`

* Ridge regression reduces large coefficients using L2 penalty
* Lasso regression can remove less important features using L1 penalty
* Helps handle overfitting and multicollinearity

---

## Final Learning Outcome

From this assignment, I learned:

* How to understand and clean real datasets
* How to visualize and analyze data
* How to build a complete ML pipeline
* How to evaluate and interpret model results

I have explained all the results and observations using plots and comments in the notebook.
