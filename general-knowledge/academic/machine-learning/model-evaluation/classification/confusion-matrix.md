# Confusion Matrix 
A confusion matrix is a table where all predicted values are separated by their class and correctness. It is call a confusion matrix because the table measures the confusion between predicted and actual classes. 

## Two Class Confusion Matrix

The table below indicates a classification task where only two distinct classes are present.
| Pre\\Act         | Positive | Negative |
| -------- | -------- | -------- |
| Positive | TP      | FP       |
| Negative | FN      | TN      |

- TP -> True Positive 
- FP -> False Positive
- TN -> True Negative 
- FN -> False Negative

## Multi-Class Confusion Matrix 

An example of a confusion matrix calculating multiple classes
| Pre\\Act | Class 1   | Class 2   | Class 3   |
| -------- | --- | --- | --- |
| Class 1        | TP | a  | b  |
| Class 2        | c  | TP | d  |
| Class 3        | e  | f | TP    |

It is common practice to calculate a given performance matrix for every class and then use the average. If we wanted to calculate a given performance matrix for class 1 the roles would look like the following 
| Pre\\Act | Class 1   | Class 2   | Class 3   |
| -------- | --- | --- | --- |
| **Class 1**        | TP | FP  | FP  |
| **Class 2**        | FN  | a | b  |
| **Class 3**        | FN | c | d    |

If the class you wanted to calculate the metric for was Class 2:
| Pre\\Act | Class 1   | Class 2   | Class 3   |
| -------- | --- | --- | --- |
| **Class 1**        | a | FN  | a  |
| **Class 2**        | FP  | TP | FP  |
| **Class 3**        | c | FN | d    |

All other [[model-evaluation|classification task evaluation]] matrix derive their values based on the confusion matrix.
- [[accuracy|Accuracy]]
- [[precision|Precision]]
- [[recall|Recall]]
- [[F1]]

**Example 1**:
| Pre\\Act | Positive | Negative |
| -------- | -------- | -------- |
| **Positive** | 428      | 29       |
| **Negative** | 100      | 290      |

**Example 2:**
| Pre\\Act | Class 1   | Class 2   | Class 3   |
| -------- | --- | --- | --- |
| **Class 1**        | 912 | 28  | 99  |
| **Class 2**        | 92  | 938 | 29  |
| **Class 3**        | 29  | 129 | 609    |


