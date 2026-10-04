# Week 4 - Supervised Learning Model Implementation

## Project Overview

This project was completed as part of my Virtual Data Science with Python internship.

For this task, I implemented a supervised learning classification model using the Breast Cancer Wisconsin Diagnostic dataset. The objective was to predict whether a tumor is malignant or benign based on numerical measurements.

## Objective

The main objectives of this project were to:

- Prepare and inspect a public dataset
- Define a binary classification problem
- Split the data into training and testing sets
- Apply feature scaling
- Train a supervised learning model
- Evaluate the model using multiple classification metrics
- Perform cross-validation
- Analyse the model coefficients
- Discuss the strengths, limitations and possible improvements of the model

## Dataset

The dataset was loaded using Scikit-learn's `load_breast_cancer()` function.

Dataset details:

- **Observations:** 569
- **Input features:** 30
- **Target classes:** Malignant and Benign
- **Malignant:** 212
- **Benign:** 357
- **Missing values:** 0
- **Duplicate rows:** 0

The target is encoded as:

- `0` = Malignant
- `1` = Benign

## Methodology

The following steps were followed:

1. Loaded the Breast Cancer Wisconsin Diagnostic dataset.
2. Inspected the dataset structure and first few records.
3. Checked for missing values and duplicate rows.
4. Separated the input features and target variable.
5. Used an 80:20 stratified train/test split.
6. Standardized the numerical features using `StandardScaler`.
7. Trained a Logistic Regression classifier.
8. Generated predictions on the test set.
9. Evaluated the model using accuracy, precision, recall and F1-score.
10. Created a confusion matrix.
11. Performed 5-fold cross-validation using a Pipeline.
12. Analysed the Logistic Regression coefficients.
13. Discussed model strengths, limitations and possible improvements.

## Model Used

### Logistic Regression

Logistic Regression was selected because this is a binary classification problem. It also provides model coefficients that can be examined to understand which features have relatively larger weights in the fitted model.

## Results

The model achieved the following results on the held-out test set:

| Metric | Result |
|---|---:|
| Accuracy | 98.25% |
| Precision | 98.61% |
| Recall | 98.61% |
| F1-Score | 98.61% |

Only **2 out of 114 test observations were misclassified**.

### Cross-Validation

5-fold cross-validation was also performed.

- Mean CV Accuracy: **98.07%**
- Standard Deviation: **0.65%**

The cross-validation results were fairly consistent across the five folds.

## Confusion Matrix

The final confusion matrix showed:

- 41 malignant cases correctly classified
- 71 benign cases correctly classified
- 1 malignant case classified as benign
- 1 benign case classified as malignant

## Feature Analysis

The Logistic Regression coefficients were examined to identify the features with the largest absolute coefficients.

The top features included:

- worst texture
- radius error
- worst concave points
- worst area
- worst radius
- worst symmetry
- area error
- worst concavity
- worst perimeter
- worst smoothness

These coefficients describe the behaviour of the fitted machine-learning model and should not be interpreted as medical cause-and-effect relationships.

## Limitations

The project has some limitations:

- The model was evaluated using one public dataset.
- Only Logistic Regression was used as the main model.
- Other classification algorithms were not compared.
- The results should not automatically be generalized to other datasets or populations.
- This project is a machine-learning exercise and is not a clinical diagnostic system.

## Possible Improvements

Future work could include:

- Comparing Logistic Regression with Random Forest, SVM and Gradient Boosting.
- Hyperparameter tuning using cross-validation.
- Evaluating ROC-AUC and plotting an ROC curve.
- Performing feature selection.
- Testing the model on an independent external dataset.

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Google Colab

## Repository Files

| File | Description |
|---|---|
| `Week_4_Supervised_Learning.ipynb` | Complete Python implementation and analysis |
| `Week_4_Supervised_Learning_Report.docx` | Detailed Week 4 project report |
| `breast_cancer_dataset.csv` | Dataset used for the project |
| `README.md` | Project overview and documentation |

## Conclusion

The project successfully implemented a supervised learning classification workflow using Logistic Regression. The model achieved 98.25% test accuracy and 98.07% mean 5-fold cross-validation accuracy. The project also included preprocessing, evaluation, error analysis, visualization and model coefficient analysis.
