Task 4: Predicting House Prices Using Boston Housing Dataset

## Objective
Build and evaluate regression models from scratch (Linear Regression, Random Forest, XGBoost) on the Boston Housing Dataset to predict house prices.


## Dataset
The dataset used is housingData.csv, which contains various housing features and the target variable MEDV (Median value of owner-occupied homes).

## Project Structure

### 1. **Data Preprocessing**
- **Load dataset** using pandas.
- **Handle missing values** by dropping rows with NaN.
- **Normalize numerical features** to scale them using Z-score normalization.
- Split the data into **training (80%)** and **testing (20%)** using train_test_split.

### 2. **Linear Regression (Implemented from Scratch)**
- A custom class LinearRegressionScratch is implemented using **Gradient Descent**.
- It updates weights and bias to minimize the **Mean Squared Error (MSE)**.
- Predictions are made using y = Xw + b.

### 3. **Random Forest (From Scratch)**
- Uses multiple **Decision Trees** built on different random samples (bootstrapped).
- Each tree is built recursively by finding the best feature and threshold to split the data.
- Final prediction is the **average of all tree outputs**.

### 4. **XGBoost (Simplified Scratch Version)**
- A boosting method that builds trees **sequentially**, each one learning from the previous model’s error.
- Each tree is trained on the **residuals** of the previous prediction.
- Final prediction is the **weighted sum** of all trees.

### 5. **Model Evaluation**
- Two metrics are used:
  - **RMSE (Root Mean Squared Error)** – Measures average prediction error.
  - **R² (R-squared)** – Measures how well the model explains variance in target.

### 6. **Feature Importance**
- For tree-based models, feature importance is calculated by **counting how often a feature is used in splits**.
- A bar chart is plotted using matplotlib to visualize most important features.


## 📌 How to Run
1. Place housingData.csv in the same directory as the notebook.
2. Run all cells sequentially.
3. The final graph shows feature importance; metrics are printed.
