# Leave One Out Cross Validation (LOOCV)
Leave-one-out cross-validation is a specialized technique that allows for a thorough assessment of a model's performance on a given dataset. It involves using each individual sample in the dataset as a validation set, while utilizing the remaining samples as the training set. This method is particularly useful for determining the generalizability of a model, as it allows for a prediction of the model's performance on unseen data. While computationally intensive, this approach is highly effective in providing a low-bias estimate of the model's true performance. It is simple to implement and requires no additional settings, however it may not be suitable for large datasets. Overall, leave-one-out cross-validation is a powerful technique within the broader category of cross-validation procedures.

However, it is important to note just how expensive LOOCV is to train. The training time for LOOCV can be defined as:
$$ CV_t \approx n \times T  $$
Where:
- $CV_t$ is the estimated run time of LOOCV 
- $n$ is the number of observations in a dataset & $n >= 1$
- $T$ is the time taken to train a model with $n-1$ observations 

For a dataset with $10,000$ observations and a model that takes roughly 2 seconds to train with $9,999$ of the observations, the training time would approximately be $5hrs$ $33min$ $20sec$. If we assume the estimate time to train the data on all observations is $T \approx 2sec$ in a k-fold validation where $k = 10$  is it would only take approximately $18sec$ for the model to finish training.  In a real world scenario the numbers would fluctuate but the large gap in time remains. This is primariliy why LOOCV is almost never used in real world scenarios where large volumes of data need to be cross-validated. 
