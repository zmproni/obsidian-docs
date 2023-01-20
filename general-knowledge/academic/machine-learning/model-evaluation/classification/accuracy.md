# Accuracy 
In the context of model evaluation, accuracy refers to the number of correct guesses over all predicted observations. 

$$ Accuracy ={ CP \over N } $$ Where:
- $CP$ is all the correctly predicted values also written as:  $TP + TN$   
- N is the total number of predictions made

This is one of the most popular metric to estimate a model's performance by, however, it has some drawbacks to consider:
- **Imbalanced Classes**: Imbalanced classes, such as 80/20 positive to negative ratio can result in misleading results. If a model were to classify all results as $TP$ then the model would score 0.8, despite getting all negative values wrong. 
- **Missclassification cost**: There are costs associated with different types of missclassification. More on this, Type 1 errors and Type 2 errors. 
- **Multi-class Problems**: Because of the different values each class might have, the accuracy's score is most affected by the dominant class. 
- **Recall** / **Precision**: It doesn't take into account the model's ability to correctly identify positive cases (Recall) or its ability to correctly identify negative cases (specificity).

**Example 1**:
| Pre\\Act | Positive | Negative |
| -------- | -------- | -------- |
| **Positive** | 428      | 29       |
| **Negative** | 100      | 290      |

1. 
$$ Accuracy = {428 + 290 \over 428 + 29 + 100 + 290} $$
2. 
$$ Accuracy \approx 0.85 $$


**Example 2:**
| Pre\\Act | Class 1   | Class 2   | Class 3   |
| -------- | --- | --- | --- |
| **Class 1**        | 912 | 28  | 99  |
| **Class 2**        | 92  | 938 | 29  |
| **Class 3**        | 29  | 129 | 609    |

1. $$ Accuracy = {912 + 938 + 609 \over 912 + 28 + 99 + 92 + 938 + 29 + 29 + 129 + 609} $$
2.  $$ Accuracy \approx 0.86 $$
