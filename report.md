# Churn Data Cleaning & EDA Report

## Files and outputs

- Cleaned dataset: `/mnt/data/churn_analysis_outputs/cleaned_data.csv`

- Preprocessed dataset (ML-ready): `/mnt/data/churn_analysis_outputs/preprocessed_data.csv`

- Saved EDA plots directory: `/mnt/data/churn_analysis_outputs`


## What I did (summary)

1. Loaded the uploaded Excel and used the first sheet as the dataset.

2. Performed exploratory data analysis: histograms, boxplots, correlation matrix.

3. Dropped columns with >50% missingness.

4. Imputed numeric missing values with the median and categorical missing with the mode (or 'Missing').

5. Capped numeric outliers using the IQR method (1.5 * IQR).

6. Produced two output files: a cleaned dataset (missing handled, outliers capped) and a preprocessed dataset ready for model building (numeric standardized and categorical variables one-hot encoded).


## Notes & rationale

- **Dropping >50% missing columns:** columns with very high missingness usually provide little signal and can complicate modeling. If you know a dropped column is important, we can instead try carefully imputing it.

- **Median imputation for numeric:** median is robust to skew and outliers.

- **Mode imputation for categorical:** preserves common categories; 'Missing' label used if none exists.

- **IQR capping for outliers:** reduces the influence of extreme values while keeping data.

- **Standardization and one-hot encoding:** produces numeric inputs suitable for most ML algorithms.


## Detected churn/target column

- Automatically detected churn-like column: **MaritalStatus**. Check that this is the column you intend to predict.


## Next steps (suggested)

1. If you want a predictive model, tell me which column is the target (churn) and whether you prefer logistic regression, tree-based models, or something else.

2. We can run feature selection, cross-validation, and build candidate models.


---

Generated programmatically. Contact me if you want further customization.
