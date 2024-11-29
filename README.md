# Build and Evaluate Logistic Regression Model

This repository provides an analysis of student performance data using binomial logistic regression and k-Nearest Neighbors (kNN) models. The goal is to predict whether a student passes or fails based on features like age, grades, and absences.

## Overview

The project consists of the following key steps:

1. **Data Loading**: Load the dataset containing student achievement data in math education.
2. **Data Transformation**: Create a pass/fail (PF) variable based on students' final grades.
3. **Logistic Regression Model**: Build a binomial logistic regression model to classify students as passing or failing.
4. **Model Refinement**: Use statistical methods to eliminate non-significant variables and identify the best model.
5. **Model Accuracy**: Evaluate the accuracy of the logistic regression model.
6. **KNN Model**: Build a kNN model for comparison and assess its accuracy.
7. **Algorithm Comparison**: Discuss the differences between logistic regression and kNN algorithms.

## 1. Data Loading

The dataset used in this project contains information on student performance in math from two Portuguese schools. It includes features such as age, prior grades, and the number of absences.

## 2. Creating Pass/Fail Variable

A new variable, `PF`, was created to classify students as "Pass" (P) or "Fail" (F) based on their final grade. This variable was later encoded as a binary outcome, where "Pass" is represented by 1 and "Fail" by 0.

## 3. Logistic Regression Model

A binomial logistic regression model was developed using selected features such as age and prior grades (`G1` and `G2`). Non-significant predictors were removed iteratively to improve the model’s performance.

## 4. Model Refinement

Three models were tested:
- The first model included `age`, `absences`, `G1`, and `G2`.
- The second model excluded `absences` based on its high p-value.
- The final model further excluded `G1` for improved statistical significance.

The second model was determined to be the best based on the Akaike Information Criterion (AIC) and the p-values of the predictors.

## 5. Model Equation

The equation for the final logistic regression model expresses the log odds of passing as a function of the student's age, first-period grade (`G1`), and second-period grade (`G2`). The coefficients were derived from the regression output.

## 6. Model Accuracy

The accuracy of the logistic regression model was calculated by comparing the predicted outcomes to the actual pass/fail results. The final model showed a higher accuracy compared to the kNN model.

## 7. KNN Model

A kNN model was built using the same features for comparison. A small test dataset was created to assess its performance. The kNN model, however, showed lower accuracy than the logistic regression model in this context.

## 8. Algorithm Comparison

### Key Differences Between Logistic Regression and kNN

| Feature              | kNN Algorithm                               | Logistic Regression                              |
|----------------------|-----------------------------------------------|--------------------------------------------------|
| **Relationships**    | Handles complex, non-linear relationships    | Assumes linear relationships                     |
| **Interpretation**   | Difficult to interpret                       | Easy to interpret                                |
| **Computational Cost**| Computationally expensive                    | Computationally efficient                        |
| **Outliers**         | Sensitive to outliers                        | Robust to outliers                               |
| **Scalability**      | Poor scalability with large datasets         | Scales well with large datasets                  |

### Conclusion

Logistic regression proved to be more accurate and interpretable than the kNN model for predicting student pass/fail outcomes in this dataset. It also demonstrated better scalability and robustness to outliers.

## Author

**Dr. Nishat Mohammad**  
Date: 03/02/2024
