The Original Dataset is subdivided in two subdatasets:
- Training set
- Test set
Sometimes the Training set is subdivided into
- Training set
- Validation set

Training set and Validation set is used to train the model and evaluate in the training stage how it performs
The Test set is the set used in the Final performance estimate test

#### K-Fold Cross Validation
The dataset is subdivided into *k* chunks, we perform the training *k* times and each time we use *k-1* chunks as training set and the one remaining chunk for validation.


high variance -> more sensivity to the input data that we give, if we train with a chunk of data we get a model and if we train with another similar chunk of data we get a complitely different model (model with high flexibility tend to have this problem like decision trees or logistic regression) -> overfitting
![](Images/Logistic%20regression%20variance.png)


high bias -> more assumptions on the input data that we get (linear regression we expect the data to be linear) -> underfitting
![](Images/Linear%20Regression%20bias.png)


#### Underfitting (high bias)
Creating a model with poor predictive ability because the model hasn't fully captured the complexity of the training data or we don't have enough training data
You can address it by:
- Increasing model complexity (e.g., adding polynomial features, using a more complex algorithm).
- Adding more features.
- Reducing regularization.
#### Overfitting (high variance)
Create a model that matches the training data so closely that the model fails to make correct predictions on new data
You can address it by:
- Increasing the amount of training data.
- Simplifying the model (e.g., reducing the number of features, using a simpler algorithm).
- Increasing regularization.
##### Regularization: Ridge regression(to reduce weights)