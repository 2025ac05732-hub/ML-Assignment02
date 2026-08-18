# Machine Learning Classification Models & Deployment Workflow
### BITS Pilani M.Tech (AIML/DSE) — Machine Learning Assignment 2

## a. Problem Statement
The objective of this assignment is to implement and evaluate multiple foundational machine learning classification algorithms on a high-dimensional dataset containing a minimum of 12 features and 500 instances. Following evaluation, an end-to-end interactive deployment dashboard is built via Streamlit and shared to enable robust, live, transparent evaluations.

## b. Dataset Description
- **Dataset Chosen**: Online Shoppers Purchasing Intention Dataset (UCI Repository)
- **Minimum Instance Requirement**: Met (1,000 generated or 12,330 standard UCI instances)
- **Minimum Feature Size**: Met (>12 feature attributes)
- **Target Feature**: `Revenue_Target` (Binary Choice: 1 if purchase occurs, 0 otherwise)
- Please download the datafile **(online_shoppers_intention.csv)** from my github repo to your local computer and then use upload option in the app to upload the file.
- Please clear cache and rerun in case you encounter sample mismatch error.

### Feature Directory Matrix
1. **Administrative**: Number of administrative pages visited by the user.
2. **Administrative_Duration**: Total time spent on administrative pages.
3. **Informational**: Number of informational pages visited.
4. **Informational_Duration**: Total time spent on informational pages.
5. **ProductRelated**: Number of product-related pages visited.
6. **ProductRelated_Duration**: Total time spent on product pages.
7. **BounceRates**: Percentage of visitors who enter the site and leave immediately.
8. **ExitRates**: Percentage of pageviews that end on that specific page.
9. **PageValues**: Average value of the page relative to transactions.
10. **SpecialDay**: Closeness of the site visit to a specific holiday/special day.
11. **OperatingSystems**: OS type indicator index.
12. **Browser**: Browser type indicator index.
13. **Region**: Geographic region index.
14. **TrafficType**: Referral traffic channel index.
15. ...
16. ..
17. .

## c. GitHub Repository Link
- `GitHub Repository Link`: [https://github.com/2025ac05732-hub/ML-Assignment02.git]
- `Live Streamlit Cloud Deployment`: [https://ml-assignment02-ltajz3jgthb2btlh6k6axy.streamlit.app/]

## d. Models Used & Comparison Matrix

| ML Model Name | Accuracy | AUC | Precision | Recall | F1 | MCC |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Logistic Regression** | 0.8816 |  0.8716 | 0.7428 | 0.3584 | 0.4835 | 0.4619 |
| **Decision Tree Classifier** | 0.8554 | 0.7295 | 0.5314 | 0.5472 | 0.5392 | 0.4535 |
| **K-Nearest Neighbor Classifier** | 0.8724 | 0.7952 | 0.6553 | 0.3689 | 0.472 | 0.4276 |
| **Naive Bayes Classifier** | 0.7805 | 0.8128 | 0.3851 | 0.7028 | 0.4975 | 0.3996 |
| **Random Forest (Ensemble)** | 0.9002 | 0.9133 | 0.7312 | 0.5612 | 0.635 | 0.5852 |

### Performance Observations & Key Takeaways

1. **Logistic Regression**: Serves as a solid baseline metric. Highly stable, clean classification boundaries but struggles slightly with non-linear feature interaction patterns.
2. **Decision Tree**: Strong ability to capture localized non-linear parameters, though prone to variance fluctuations on smaller cuts of validation feature splits.
3. **kNN**: Dependent on scaling choices. When distance distributions are uniformized via standard preprocessing, it models neighbors efficiently but slows down relative to size scaling.
4. **Naive Bayes**: Shows strong performance on Recall metrics but drops significantly on Precision due to its rigid conditional independence feature assumptions.
5. **Random Forest (Ensemble)**: Establishes the **Overall Winner** profile on this dataset. It achieves the highest validation AUC and MCC by combining multiple localized decorrelated tree distributions to reduce variance.
