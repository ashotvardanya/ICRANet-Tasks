# Pre-interview Task

## Task 1: Data Cleaning and EDA

**Objective:**
Clean the data and perform exploratory data analysis (EDA) on VOU multifrequency data and redshift values. Link source names with their redshift values.

### Steps Completed:

1. **Data Association:**
    - Matched source names from VOU data with redshift values.
2. **Data Cleaning:**
    - Documented the cleaning steps.
    - We could have removed either upper, lower bound or error because they are linearly correlated. 
3. **EDA and Redshift Analysis:**
    - Analyzed data properties and patterns.
    - Generated summary statistics.
    - Created visualizations (e.g., histograms, scatter plots, box plots).

### Data Info

> VOU data: aggregation of blazars, frequency (electromagnetic frequency), nufnu (flux), nufnu lower/upper (error bounds), start/end-time (detection time), flag (data point status), catalog (data source), nufnu err (derived error).

### Data Preprocessing Steps
- **Filtered nufnu Values:** Removed rows with nufnu ≤ 0.
- **Filtered nufnu Range:** Kept rows where nufnu is within nufnu_lower and nufnu_upper.
- **Removed ‘UL’ Flag:** Excluded rows with flag ‘UL’.

### Conclusions
- Many data points lack redshift values.
- Redshift values are higher closer to 0.
- Blazars with low nufnu and low frequency have lower redshift values.

## Task 2: Regression Analysis

**Objective:** Build and evaluate regression models to predict tips using the `Tips` Seaborn dataset.

**Approach:**
1. **Data Preprocessing:**
   - Standardize numerical features.
   - One-hot encode categorical features.

2. **Model Building:**
   - Linear Regression.
   - Decision Tree Regression.
   - Deep Neural Network Regression.
   - Stacked Regression.

3. **Evaluation:**
   - Use Mean Squared Error (MSE) and Mean Absolute Error (MAE).
   - Discuss impact of loss functions on skewed data.

4. **Conclusion:**
   - Compare model performance.
   - Explain choice of models, evaluation metrics, and loss functions.

## Code Summary

### Data Preprocessing
- Standardized numerical features and one-hot encoded categorical features using `StandardScaler` and `OneHotEncoder`.
- Split the data into training and test sets.

### Model Building
- Built and trained four models: Linear Regression, Decision Tree Regression, Deep Neural Network Regression, and Stacked Regression.
- Used Mean Squared Error (MSE) and Mean Absolute Error (MAE) as evaluation metrics.

### Results
- Linear Regression:
  - MSE: 0.703, MAE: 0.667
- Decision Tree Regression:
  - MSE: 1.392, MAE: 0.878
- Deep Neural Network Regression:
  - MSE: 0.728, MAE: 0.689
- Stacked Regression:
  - MSE: 0.682, MAE: 0.672

### Conclusion
- The Stacked Regression model performed the best in terms of MSE and MAE, followed by the Deep Neural Network Regression model.
- These models can be used to predict tips based on the provided dataset.


---

Ashot Vardanyan
