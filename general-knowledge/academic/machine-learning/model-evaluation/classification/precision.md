# Precision 
It indicates how well the model can identify positive instances in the data. Precision answers the question: how many positive predictions made were correct?

$$ Precision = { TP \over TP + FP }$$
Where:
- $TP$ -> True Positive 
- $FP$ -> False Positive

Easy way to differentiate with its counterpart [[recall]] is:
	Recall Real,
	Precision Predicted.

Precision is used when the goal is to minimize the number of false positives, it measures the ability of the model to correctly identify positive instances. Precision is particularly important when the cost of a false positive is high, such as in the email spam filter, where a false positive could result in important emails being blocked.