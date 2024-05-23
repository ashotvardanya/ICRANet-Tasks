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



---

Ashot Vardanyan
