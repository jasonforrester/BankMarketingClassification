# Bank Marketing Campaign - Comparing Classifiers

Evaluation Metrics
To assess the performance of these classifiers, we need clearly defined evaluation criteria. As highlighted in the study "Using Data Mining for Bank Direct Marketing: An Application of the CRISP-DM Methodology" by Moro and Laureano, the AUC-ROC curve is an excellent metric for this business context. The AUC-ROC plots the True Positive Rate (TPR) against the False Positive Rate (FPR), providing insight into the model's ability to identify true buyers while minimizing false positives. This is especially relevant for optimizing resource allocation during campaigns and enhancing profitability.

Additional metrics—Accuracy, F1 Score, Precision, and Recall—will offer a more comprehensive understanding of each model's performance. Furthermore, runtime will be tracked to evaluate the trade-off between accuracy and computational efficiency.

## Key Findings
One important characteristic of the dataset is its severe class imbalance, with approximately 89% of the responses being "no" and only 11% "yes." Despite this challenge, the analysis identified logistic regression and decision trees as the most effective models. Notably:

Logistic regression emerged as the top-performing model, achieving an AUC-ROC score of 65% and an F1 score of 25%.
Decision trees followed closely with an AUC-ROC of 64.7%, though their F1 score was considerably lower at 4.5%.
Due to its high computational demands, SVM was evaluated on a reduced dataset of 5,000 observations. Even with grid search optimization, it required significant runtime, limiting its practicality for large-scale data.
Overall, logistic regression stands out as the best option for predicting campaign success, balancing reasonable accuracy with computational efficiency.

## Areas for Further Investigation
Several avenues exist for refining the analysis and improving model performance:

Parameter Optimization: Conduct a deeper exploration of hyperparameters for logistic regression and decision trees.
Addressing Class Imbalance: Investigate techniques such as oversampling, undersampling, or synthetic data generation to balance the dataset.
Feature Engineering: Incorporate additional features from the dataset, such as macroeconomic indicators, seasonal trends (e.g., months and days), and other relevant variables.
Handling Missing Data: Explore strategies to impute, replace, or remove "unknown" values in the dataset.
Focused Feature Analysis: Based on preliminary findings, the variable poutcome (previous campaign outcome) shows strong predictive power. Additional predictors with a high ratio of "yes" to "no" should be sampled and included in future iterations.
Data Filtering: As suggested in prior research, excluding inconclusive or ambiguous contacts from the dataset may enhance model accuracy.
These next steps could further refine the predictive models, yielding even better insights for future telemarketing campaigns.


## How to Use
1. Clone this repository.
2. Place the dataset (`bank-additional-full.csv`) into the `data/` folder if not already present.
3. Open and run the Jupyter notebook in the `notebooks/` folder: `prompt_IIIv2.ipynb`.

