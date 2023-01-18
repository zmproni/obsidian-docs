# Choosing Model Evaluation Techniques 

> Model evaluation the act of measuring of the model's performance given the business goal and modelling technique 

Mapping problem to machine learning task -> Evaluating model -> Validating model

| Model evaluation                                                                     | Model validation                                             |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------ |
| Refers to the measurement of the scoring metrics for a Model on a particular dataset | To check the fitness of the model given its intended purpose |

# Important terminology

### Model Evaluation 
With the aid of model performance metrics like F1 score, Precision, Recall and Accuracy (Classification Metrics) we can determine the performance of a model against a given dataset. 

### Model Validation
Makes sure the model evaluation is correct through cross-validation techniques and it is suitable for the purpose of the business needs. It is meant to determine if a model over-fits or under-fits. 

<img src="https://imgur.com/vx1Jwo2.png" width=100% >

# Classification Models 
Classification evaluation metrics focus on determining the correctness of a model to classify the observation's respective tasks. 

The following are the techniques used to evaluate classification models:
- [[confusion-matrix|Confusion Matrix]]
- [[accuracy|Accuracy]] 
- [[precision|Precision]] 
- [[recall|Recall]] 
- [[F1]] 
- ROC-AUC

# Regression Models
Regression tasks focus on predicting a continuous value such as the house price based on its facilities, neighbourhood, size, etc. 

Techniques used: 
- [[R2|R-squared (R2)]] 
- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)

# Probability Models 
Probability models are useful for both classification and scoring tasks. Probability models are models that both decide if an item is in a given class and return an estimated probability (or confidence) of the item being in the class. The modelling techniques of logistic regression and decision trees are fairly famous for being able to return good probability estimates.

Techniques used:
- Receiver operating characteristic curve (ROC Curve)
- Log Likelyhood
- Deviance 
- Akaike Information Criterion (AIC)

