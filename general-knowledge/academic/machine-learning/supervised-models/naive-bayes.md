# Naive Bayes 
It is a statistical model that computes the likely-hood of A to happen given independent variables B.

It is based on Bayes' law. It is called naive because it is a naive notion to consider the probability of several predictors to be completely independent. 
$$P(A|B) = {P(B|A)\text{ }P(A) \over P(B)}$$
This is read as: The probability of A given B is equal to the probability of B given A times the probability of A, over the probability of B.

**Example**:
Based on the following table, calculate the probability of whether the players will play given that the weather is sunny.

| Weather  | Play |
| -------- | ---- |
| Sunny    | No   |
| Overcast | Yes  |
| Rainy    | Yes  |
| Sunny    | Yes  |
| Sunny    | Yes  |
| Overcast | Yes  |
| Rainy    | No   |
| Rainy    | No   |
| Sunny    | Yes  |
| Rainy    | Yes  |
| Sunny    | No   |
| Overcast | Yes  |
| Overcast | Yes  |
| Rainy    | No   |

**Explanation**
1. Formulate equation 
$$P(Yes|Sunny) = {P(Sunny|Yes)\text{ }P(Yes)\over P(Sunny)}$$
2. Create a frequency table for when condition is true
| Play    | Sunny | Not Sunny | $\sum$|
| ------- | ----- | --------- |---|
| **Yes** | 3     | 6         | 9|
| **No**  | 2     | 3         |5 |
| $\sum$  | 5     | 9         ||


3. Calculate $P(A)$, $P(B)$, $P(B|A)$
	$P(Yes)$
$$P(Yes) = {9 \over 14}$$
$$P(Yes) \approx 0.643 $$
	$P(Sunny)$
$$P(Sunny) = {5 \over 14}$$
$$P(Sunny) \approx 0.357$$
	$P(Sunny|Yes)$
	$$P(Sunny|Yes) = {3 \over 9}$$
	$$P(Sunny|Yes) \approx 0.333$$
4. Calculate $P(Yes|Sunny)$
$$P(Yes|Sunny) = {0.333 * 0.643 \over 0.357}$$
$$P(Yes|Sunny) \approx 0.6$$

Review written notes for multivariate question and solution. Note, when calculating the result it is better to use fractions rather than their rounded decimal form as it can lead to inaccuracies with the final result. 