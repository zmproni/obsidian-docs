# Cross-validation Methods
Cross-validation is a technique where data is divided such that it is possible to use the various subsets of data to train and evaluate the performance of a model. Cross-validation allows users to assess the performance of a model, tune mode parameters, help decide which model performs best and even help train a model. There are various techniques to cross-validation and each have their benefits and downsides. The specific ones that will be discussed are:
- **Hold-out validation**
- **K-fold cross validation**
- **Stratified K-fold cross validation**
- **Repeated Stratified K-fold cross validation**
- **Leave One Out Cross Validation (LOOCV)**
There are more cross validation techniques, however we will only tackle the ones mentioned above (perhaps more will be added in the future).  

## Hold-out validation
![[holdout.png]]
Hold out validation refers to splitting the dataset into two groups, a test group and a train group. The train group is data that will be used to train a machine learning model and the test group is used to check how  model predicts values it wasn't trained on.  
  
Theoretically, this should make the results of the model evaluation much more accurate than just training the whole dataset and testing using the same dataset. The standard approach to splitting the dataset into training and testing is 70-30 where 70% of the data becomes the training data and the rest becomes testing, 80-20 is another popular approach.  
  
This approach is generally not seen as a true cross-validation technique but it is used in most scenarios in conjunction to other cross-validation methods as shown in the following sections.  
 
Pros:
- Simple to implement: Data is split into two sets: training and testing
- Provides model evaluation based on data the model hasn't been. trained on preventing test data overfitting.
- Can be used in combination with other techniques to get clearer estimates of a model's performance. 
Cons:
- Is sensitive to random splits: This can cause imbalance in the data as it is not an accurate representation of the population anymore leading to overfitting the training data
- Suffers from small sample sizes 
- The test set is only used once, so it doesn't provide much information  on how it will generalise to new unseen data

Though severe these issues can be circumvented by applying the following methodologies:
- Stratification: Stratification when splitting the dataset helps maintain the population distribution between the train and test sets. 
- Using other cross-validations techniques on the train set to see how the model will react to unseen data during the training process and improve the final trained model. 

## K-Fold validation
![[kfold-crossval.png]]
In k-fold cross-validation, the original dataset is divided into k sub-parts or folds. For each iteration, one fold is selected as the validation set, while the remaining $k-1$ folds are used as the training set. This process is repeated k times until each fold has been used as the validation set.  

During the model training phase we can validate the performance of the model and tune its hyper parameters to get the best possible outcome. By repeating the training and validation for each of the splits we can observe how the model reacts to unseen data, which is a better indication of it's true performance. 

The method has a single parameter, k, which refers to the number of groups that the dataset is to be split into. 

![[kfold.png]]

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

## Stratified K-Fold validation
![[stratified-kfold.png]]
Stratified K-Fold cross validation takes into consideration the issue of random population splits that can introduce issues with class representations and solves it with semi-random splits where each split contains the same class distribution. Models trained with dataset splits that have not been stratified can suffer from situations where certain folds are dominated by a single class. This leads to bias in the evaluation of a model's performance  as the model is not exposed to all the classes in the training set. 

Pros:
- Has all the advantages of k-fold.
- Represents the accurate distribution of target class for each split. 

Cons:
- It is still computationally expensive.

## Repeated Stratified K-fold cross validation
![[multiple-kfold.png]]
Repeated k-fold cross-validation is a technique used to evaluate the performance of a model when the dataset is large. It is a variation of k-fold cross-validation where the k-fold procedure is repeated multiple times with different random partitions of the data where only one fold is validated per procedure.

However, when the dataset is large, k-fold cross-validation can be computationally expensive and may not be the most efficient method.

Pros:
-   By repeating the k-fold procedure multiple times with different random partitions of the data, it provides a more robust estimate of the model's performance.
-   It is useful when working with large datasets and imbalanced target variables.
Cons:
-   The results can be dependent on the specific partition of the data into k-folds and the number of repetitions.
-   It is not always clear what value of k to use and how many repetitions to make.
-   It can be sensitive to the order of the data, which may cause bias in the selection of the training and validation sets. So it's important to shuffle the data before dividing it into repeated k-folds

## Leave One Out Cross Validation (LOOCV)
Leave-one-out cross-validation is a specialized technique that allows for a thorough assessment of a model's performance on a given dataset. It involves using each individual sample in the dataset as a validation set, while utilizing the remaining samples as the training set. This method is particularly useful for determining the generalizability of a model, as it allows for a prediction of the model's performance on unseen data. While computationally intensive, this approach is highly effective in providing a low-bias estimate of the model's true performance. It is simple to implement and requires no additional settings, however it may not be suitable for large datasets. Overall, leave-one-out cross-validation is a powerful technique within the broader category of cross-validation procedures.

However, it is important to note just how expensive LOOCV is to train. The training time for LOOCV can be defined as:
$$ CV_t \approx n \times T  $$
Where:
- $CV_t$ is the estimated run time of LOOCV 
- $n$ is the number of observations in a dataset & $n >= 1$
- $T$ is the time taken to train a model with $n-1$ observations 

For a dataset with $10,000$ observations and a model that takes roughly 2 seconds to train with $9,999$ of the observations, the training time would approximately be $5hrs$ $33min$ $20sec$. If we assume the estimate time to train the data on all observations is $T \approx 2sec$ in a k-fold validation where $k = 10$  is it would only take approximately $18sec$ for the model to finish training.  In a real world scenario the numbers would fluctuate but the large gap in time remains. This is primariliy why LOOCV is almost never used in real world scenarios where large volumes of data need to be cross-validated. 

## Notes
[Link](https://www.canva.com/design/DAFXkt4S488/gsfnJYQrFMNi4_Q5NEFnCQ/edit) to the worspace used to create the graphics. 