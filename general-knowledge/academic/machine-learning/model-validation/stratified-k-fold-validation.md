# Stratified K-Fold validation
![[stratified-kfold.webp]]
Stratified K-Fold cross validation takes into consideration the issue of random population splits that can introduce issues with class representations and solves it with semi-random splits where each split contains the same class distribution. Models trained with dataset splits that have not been stratified can suffer from situations where certain folds are dominated by a single class. This leads to bias in the evaluation of a model's performance  as the model is not exposed to all the classes in the training set. 

Pros:
- Has all the advantages of k-fold.
- Represents the accurate distribution of target class for each split. 

Cons:
- It is still computationally expensive.
