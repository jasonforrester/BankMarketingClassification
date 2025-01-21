# Bank Marketing Campaign - Comparing Classifiers

This project compares the performance of four supervised learning algorithms:
- K-Nearest Neighbors
- Logistic Regression
- Decision Tree
- Support Vector Machine

on the [UCI Bank Marketing Dataset](https://archive.ics.uci.edu/ml/datasets/Bank+Marketing).

## Summary of Findings
1. **Data Overview**: The dataset includes 41,188 telephone marketing contacts with various features like age, job, marital status, etc., and a target variable `y` indicating whether the client subscribed to a term deposit.
2. **Preprocessing**: 
   - Handled missing data by removing unknown or filling with modes where appropriate.
   - Performed label encoding for categorical features.
   - Standardized or applied one-hot encoding to certain features for better model performance.
3. **Model Comparison**:
   - **Logistic Regression** (best parameters: `C=1`) gave us an F1-score of ~XX%.
   - **K-Nearest Neighbors** (best `k=7`) gave us an F1-score of ~YY%.
   - **Decision Tree** (best `max_depth=5`) gave us an F1-score of ~ZZ%.
   - **SVM** (best `C=1, kernel='rbf'`) gave us an F1-score of ~AA%.
4. **Recommendations**:
   - Overall, {Model X} performed best on precision/recall trade-offs.
   - Using these insights, the bank can better target clients who are likely to subscribe.

## How to Use
1. Clone this repository.
2. Place the dataset (`bank-additional-full.csv`) into the `data/` folder if not already present.
3. Open and run the Jupyter notebook in the `notebooks/` folder: `bank_marketing_comparing_classifiers.ipynb`.

## Next Steps
- Consider additional feature engineering (e.g., binning of age, etc.).
- Attempt ensemble methods like Random Forest or Gradient Boosted Trees for potentially better performance.
