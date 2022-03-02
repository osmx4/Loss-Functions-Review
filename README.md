import numpy as np

## Regressions Losse functions
#1 MSE
def mse(predictions, targets):
    differences = predictions - targets
    differences_squared = differences ** 2
    mean_of_differences_squared = differences_squared.mean()
    mse_val = np.sqrt(mean_of_differences_squared)
    return mse_val

#2 MAE
def mae(predictions, targets):
    differences = predictions - targets
    absolute_differences = np.absolute(differences)
    mean_absolute_differences = absolute_differences.mean()
    return mean_absolute_differences

## Classification losses functions
#1 Multi class SVM Loss
def maxloss1(x1, x2, x3):
    maxvalue1 = max(0,(x2-x1)+1) + max(0, (x3-x1)+1)
    print(maxvalue1)
# Press the green button in the gutter to run the script.

def cross_entropy(predictions, targets, epsilon=1e-10):
    predictions = np.clip(predictions, epsilon, 1. - epsilon)
    N = predictions.shape[0]
    ce_loss = -np.sum(np.sum(targets * np.log(predictions + 1e-5)))/N
    return ce_loss

if __name__ == '__main__':

    y_hat = np.array([0.000, 0.166, 0.333])
    y_true = np.array([0.000, 0.254, 0.998])
    mse_val = mse(y_hat, y_true)
    print("rms error is: " + str(mse_val))

    mae_val = mae(y_hat, y_true)
    print("mae error is: " + str(mae_val))
    x1, x2, x3 = ([1.49, -0.39, 4.21])
    lossvaluee= maxloss1(x1, x2, x3)

    predictions = np.array([[0.25, 0.25, 0.25, 0.25],
                            [0.01, 0.01, 0.01, 0.96]])
    targets = np.array([[0, 0, 0, 1],
                        [0, 0, 0, 1]])
    cross_entropy_loss = cross_entropy(predictions, targets)
    print("Cross entropy loss is: " + str(cross_entropy_loss))


