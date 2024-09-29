# Coursera_Machine_learning
We want to calculate the mean (mu) and variance (var) manually using the formula instead of relying on NumPy's built-in functions.
we must know the formula for calculating the value of mean and variance, so that we can implement it in our code.
In exercise 1, mu = np.sum(X, axis=0) / m: This computes the mean by summing all the elements in each column and dividing by the number of rows (examples).

var = np.sum((X - mu) ** 2, axis=0) / m: This computes the variance by first subtracting the mean from each element, squaring the result, summing these squares, and dividing by the number of rows.

We will beimplementing the formula which is suggested in the assigment in both of the exercises.
In exercise 2, To implement the function for selecting the best threshold (epsilon) and calculating the F1 score, you need to manually compute:

True Positives (TP): The number of times the model predicted an outlier (1) and it was actually an outlier (1).
False Positives (FP): The number of times the model predicted an outlier (1) but it wasn't (0).
False Negatives (FN): The number of times the model predicted non-outlier (0) but it was actually an outlier (1).
Then, based on these values, you can compute Precision and Recall using the formulas provided in the assignment.

Predictions: We predict an outlier if the value is less than the threshold (epsilon).

predictions = (p_val < epsilon).astype(int) makes a binary array where values are 1 (outlier) if the corresponding p_val is less than epsilon, and 0 otherwise.
TP, FP, FN Calculations:

True positives: when both predictions and y_val are 1.
False positives: when predictions is 1 but y_val is 0.
False negatives: when predictions is 0 but y_val is 1.
Precision and Recall: We handle division by zero by checking if the denominator is zero to avoid runtime errors.

F1 Score Calculation: We compute the F1 score only if both precision and recall are not zero.
Please read the formula's first before going through the codes for easier understanding.
