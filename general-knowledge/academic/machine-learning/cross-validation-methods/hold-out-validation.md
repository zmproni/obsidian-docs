# Hold-out validation
![[holdout.webp]]
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
