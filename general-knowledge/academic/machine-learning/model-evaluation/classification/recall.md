# Recall 
Recall answers the question: how many positive values were correctly predicted. 
$$Recall = {TP \over TP + FN }$$

Where:
- $TP$ is true positive 
- $FN$ is false negative

Easy way to differentiate with its counterpart [[precision]] is:
	Recall Real,
	Precision Predicted.

Recall is used when the goal is to minimise the number of false negatives, it measures the ability of the model to correctly identify all relevant instances. Recall is particularly important when the cost of missing a positive instance is high, such as in medical diagnosis, where failing to identify a disease could have severe consequences.

**Example 1**:

| Pre\\Act | Positive | Negative |
| -------- | -------- | -------- |
| **Positive** | 428      | 29       |
| **Negative** | 100      | 290      |

Calculate recall: 
1. Input values $$Recall = {428 \over 428 + 100} $$
2. Calculate $$Recall \approx 0.81$$

**Example 2:**
| Pre\\Act | Class 1   | Class 2   | Class 3   |
| -------- | --- | --- | --- |
| **Class 1**        | 912 | 28  | 99  |
| **Class 2**        | 92  | 938 | 29  |
| **Class 3**        | 29  | 129 | 609    |

Calculate recall for Class 3: 
1. Input values $$Recall = {609 \over 609 + 99 + 29 }$$
2. Calculate $$Recall \approx 0.82$$


