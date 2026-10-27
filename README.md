# Ecommerce Customer Spending Prediction

## Overview

This project uses **Multiple Linear Regression** to predict the yearly amount spent by e-commerce customers based on their session length, time spent on the app and website, and membership duration.

The project demonstrates a basic machine learning workflow, including exploratory data analysis, feature selection, model training, prediction, and evaluation using Python and Scikit-learn.

## Objectives

- Explore customer data and relationships between features.
- Perform exploratory data analysis and visualization.
- Implement multiple linear regression.
- Understand model coefficients and the intercept.
- Evaluate model performance using regression metrics.

## Dataset

The project uses the Ecommerce Customers dataset, which contains customer information and usage statistics.

### Features used

| Feature | Description |
|---|---|
| Avg. Session Length | Average customer session length |
| Time on App | Time spent using the app |
| Time on Website | Time spent using the website |
| Length of Membership | Duration of customer membership |

**Target variable:** `Yearly Amount Spent`

The dataset also contains `Email`, `Address`, and `Avatar`. These columns are excluded from the model.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Project Structure

```text
Linear Regression in Python/
├── data/
│   └── ecommerce.csv
├── notebooks/
│   └── linear-reg-with-python.ipynb
├── README.md
└── .gitignore
```

## Methodology

### 1. Data Preparation
- Load the dataset using Pandas.
- Inspect the dataset structure and descriptive statistics.
- Select relevant numerical features and the target variable.

### 2. Exploratory Data Analysis
- Use a joint plot to explore the relationship between membership duration and yearly spending.
- Use pair plots to examine relationships among numerical variables.

### 3. Train-Test Split

Split the dataset into training and testing sets:

- Training data: 70%
- Testing data: 30%
- Random state: 42

### 4. Model Training

Train a multiple linear regression model using Scikit-learn's `LinearRegression` estimator.

### 5. Prediction and Visualization

Generate predictions on the test dataset and visualize predicted values against actual values.

### 6. Model Evaluation

Evaluate the model using four metrics:

- **Mean Squared Error (MSE):** Average of squared prediction errors.
- **Mean Absolute Error (MAE):** Average absolute difference between actual and predicted values.
- **Root Mean Squared Error (RMSE):** Square root of MSE, which penalizes larger errors more heavily.
- **R² Score:** Measures how well the model explains variation in the target relative to a mean-prediction baseline.

## Results

The model was evaluated on the held-out test dataset using four regression metrics.

| Metric | Result |
|---|---:|
| Mean Squared Error (MSE) | 103.9155 |
| Mean Absolute Error (MAE) | 8.4261 |
| Root Mean Squared Error (RMSE) | 10.1939 |
| R² Score | 0.9809 |

### Interpretation

- **MSE:** The average squared prediction error is approximately 103.92.
- **MAE:** Predictions differ from actual yearly spending by approximately 8.43 units on average.
- **RMSE:** The root mean squared prediction error is approximately 10.19 units.
- **R² Score:** The model explains approximately 98.09% of the variation in yearly spending on the test dataset relative to a mean-prediction baseline.

These results indicate that the linear regression model fits this dataset well on the held-out test set. However, performance on unseen data should be validated further before drawing broader conclusions.

## Key Learnings

- Understanding supervised learning and regression.
- Exploring data using visualizations.
- Preparing training and testing datasets.
- Fitting a multiple linear regression model.
- Interpreting coefficients and the intercept.
- Evaluating model performance using regression metrics.

## How to Run

1. Clone or download the repository.
2. Install the required dependencies:

   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn jupyter
   ```

3. Navigate to the project directory and start Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

4. Open `notebooks/linear-reg-with-python.ipynb` and run the cells in order.

Ensure the dataset is available at `data/ecommerce.csv` relative to the project root. The notebook's relative path should match the folder from which it is run.

## Acknowledgements

This project was developed as part of my machine learning learning journey using a practical e-commerce dataset. 

Dataset: Ecommerce Customers dataset - https://www.kaggle.com/datasets/kolawale/focusing-on-mobile-app-or-website?resource=download 