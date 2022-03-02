# Loss-Functions-Review
Loss functions in machine Learning
Mainly, loss functions can be classified into two major categories considering the training task, that are:
	Regression losses 
There are various factors involved in choosing a loss function for specific problem such as type of machine learning algorithm chosen, ease of calculating the derivatives and to some degree the percentage of outliers in the data set.
	Mean Square Error Loss
MSE=(∑_(i=1)^n▒〖(y_i-y ̂_i )^2  〗)/n
The Mean square error is measured as the average of squared difference between predictions and actual observations.
	Mean Absolute Error
Mean absolute error is measured as the average of sum of absolute differences between predictions and actual observations
MAE=(∑_(i=1)^n▒〖|y_i-y ̂_i | 〗)/n

	Classification Losses
	Multi class SVM Loss
The score of the correct category should be greater than sum of scores of all incorrect categories by some safety margin (usually one). And hence this loss is used for maximum-margin classification, most notably for support vector machines. Although not differentiable, it’s a convex function which makes it easy to work with usual convex optimizers used in machine learning domain.
SVM Loss=∑_(j≠y_i)▒〖max(0,s_j-〖s_y〗_i+1) 〗
Example: Consider an example where we have three training examples and three classes to predict: 1) Dog, 2) cat; and 3) Horse. Below the values predicted by our algorithm for each of the classes [2]: 
 
* This table and pictures are brough from [2]
	Negative Log Likelihood Function (Cross Entropy)
The value of this loss function increases as the predicted probability diverges from the actual label.
NLL(Cross Entropy Loss)= -(y_i  log⁡(y ̂_i )+(1-y_i )  log⁡〖(1-y ̂_i 〗)
Notice that when actual label is 1 (y(i) = 1), second half of function disappears whereas in case actual label is 0 (y(i) = 0) first half is dropped off. In short, we are just multiplying the log of the actual predicted probability for the ground truth class. 

References: 
1] Bishop, Christopher M., and Nasser M. Nasrabadi. Pattern recognition and machine learning. Vol. 4, no. 4. New York: springer, 2006.
2] https://towardsdatascience.com/common-loss-functions-in-machine-learning-46af0ffc4d23, last visited Feb 25, 2022. 
Loss functions in machine Learning
Mainly, loss functions can be classified into two major categories considering the training task, that are:
	Regression losses 
There are various factors involved in choosing a loss function for specific problem such as type of machine learning algorithm chosen, ease of calculating the derivatives and to some degree the percentage of outliers in the data set.
	Mean Square Error Loss
MSE=(∑_(i=1)^n▒〖(y_i-y ̂_i )^2  〗)/n
The Mean square error is measured as the average of squared difference between predictions and actual observations.
	Mean Absolute Error
Mean absolute error is measured as the average of sum of absolute differences between predictions and actual observations
MAE=(∑_(i=1)^n▒〖|y_i-y ̂_i | 〗)/n

	Classification Losses
	Multi class SVM Loss
The score of the correct category should be greater than sum of scores of all incorrect categories by some safety margin (usually one). And hence this loss is used for maximum-margin classification, most notably for support vector machines. Although not differentiable, it’s a convex function which makes it easy to work with usual convex optimizers used in machine learning domain.
SVM Loss=∑_(j≠y_i)▒〖max(0,s_j-〖s_y〗_i+1) 〗
Example: Consider an example where we have three training examples and three classes to predict: 1) Dog, 2) cat; and 3) Horse. Below the values predicted by our algorithm for each of the classes [2]: 
 
* This table and pictures are brough from [2]
	Negative Log Likelihood Function (Cross Entropy)
The value of this loss function increases as the predicted probability diverges from the actual label.
NLL(Cross Entropy Loss)= -(y_i  log⁡(y ̂_i )+(1-y_i )  log⁡〖(1-y ̂_i 〗)
Notice that when actual label is 1 (y(i) = 1), second half of function disappears whereas in case actual label is 0 (y(i) = 0) first half is dropped off. In short, we are just multiplying the log of the actual predicted probability for the ground truth class. 

References: 
1] Bishop, Christopher M., and Nasser M. Nasrabadi. Pattern recognition and machine learning. Vol. 4, no. 4. New York: springer, 2006.
2] https://towardsdatascience.com/common-loss-functions-in-machine-learning-46af0ffc4d23, last visited Feb 25, 2022. 
