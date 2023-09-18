# Credit Risk Classification Analysis

In this project, machine learning techniques were employed to assess a dataset containing historical lending activities of a peer-to-peer lending services company. The primary objective was to develop a model capable of accurately classifying the creditworthiness of borrowers.

## Analysis Overview
The analysis encompassed various factors, including:

- Loan size
- Interest rate
- Borrower's income
- Debt-to-income ratio
- Number of accounts held by the borrower
- Derogatory marks against the borrower
- Total debt

The dataset consisted of 77,536 data points and was divided into training and testing sets. The training set was utilized to construct an initial logistic regression model, denoted as Logistic Regression Model 1, employing the `LogisticRegression` module from [scikit-learn](https://scikit-learn.org/stable/index.html). Subsequently, Logistic Regression Model 1 was applied to the testing dataset to assess its performance in classifying loans as low-risk or high-risk.

The initial model drew from a dataset comprising 75,036 low-risk loan data points and 2,500 high-risk data points. To address the imbalance and ensure equal representation in the training data, the `RandomOverSampler` module from [imbalanced-learn](https://imbalanced-learn.org/dev/index.html) was employed. This resampling process generated 56,277 data points for both low-risk (0) and high-risk (1) loans, preserving the characteristics of the original dataset.

The resampled data was subsequently employed to construct a new logistic regression model, referred to as Logistic Regression Model 2. The objective of this model was identical to its predecessor—to classify loans in the testing set as either low-risk or high-risk.

## Results

Logistic Regression Model 1:

- Precision: 93% (averaged; 100% precision for low-risk loans, 87% for high-risk loans)
- Accuracy: 94%
- Recall: 95% (averaged; 100% recall for low-risk loans, 89% for high-risk loans)

Logistic Regression Model 2:

- Precision: 93% (averaged; 100% precision for low-risk loans, 87% for high-risk loans)
- Accuracy: 100%
- Recall: 100%

## Summary
Logistic Regression Model 2 exhibits a reduced likelihood of producing false negatives, making it more reliable in identifying high-risk loans. However, it is noteworthy that Logistic Regression Model 2 predicts slightly more false positives (misclassifying low-risk loans as high-risk). If the primary goal is to assess the likelihood of high-risk loans, neither model achieves precision above 90%. Nonetheless, Logistic Regression Model 2 outperforms the first model in terms of accuracy and recall, making it the preferred choice due to its high overall accuracy and recall rates.

