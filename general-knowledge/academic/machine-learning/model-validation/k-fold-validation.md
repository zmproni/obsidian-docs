# K-Fold validation
![[kfold-crossval.webp]]
In k-fold cross-validation, the original dataset is divided into k sub-parts or folds. For each iteration, one fold is selected as the validation set, while the remaining $k-1$ folds are used as the training set. This process is repeated k times until each fold has been used as the validation set.  

During the model training phase we can validate the performance of the model and tune its hyper parameters to get the best possible outcome. By repeating the training and validation for each of the splits we can observe how the model reacts to unseen data, which is a better indication of it's true performance. 

The method has a single parameter, k, which refers to the number of groups that the dataset is to be split into. 

![[kfold.webp]]

Cross-validation is mainly used to estimate a model's performance on unseen data. This means that a limited dataset is used to estimate how the model is likely to perform when making predictions on data that was not used during the training of the model.

It is a popular method because it is easy to understand, and it commonly results in a less biased or more realistic estimate of the model's performance, compared to other methods, such as a simple train-test split.

Pros:
-   K-fold cross-validation provides an estimate of the model's performance on unseen data, which is more indicative of its true performance.
-   It helps to overcome the problem of having a small test set, which may not be representative of the population.
-   By averaging the performance of the model over k iterations, it reduces the variance of the estimate of the model's performance.
-   It can also be used to tune the parameters of a model by training on different subsets of the data and selecting the parameters that result in the best performance on the held-out subset.

Cons:
-   It is computationally expensive, especially when k is large or the dataset is large.
-   The results can be dependent on the specific partition of the data into k-folds.
-   It can be sensitive to the order of the data, which may cause bias in the selection of the training and validation sets, so, it's important to shuffle the data before dividing it into k-folds
-   It is not always clear what value of k to use.
