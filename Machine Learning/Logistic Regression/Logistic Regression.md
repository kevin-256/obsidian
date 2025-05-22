Logistic regression is a supervised machine learning algorithm used for classification tasks where the goal is to predict the probability that an instance belongs to a given class or not.

*m* = Number of training Examples
x<sub>1</sub>,x<sub>2</sub>...x<sub>n</sub> = Features
y<sub>1</sub>,y<sub>2</sub>...y<sub>n</sub> = Target
(x, y) = One training example
(x<sup>(i)</sup>,y<sup>(i)</sup>) = i-th training example (one row of the table)

Instead of using a linear function like **Regression**, **Logistic Regression** use a function called **Sigmoid function** or **Logistic Function**:
g(z) = 1/(1+e<sup>-z</sup>) = 1/(1+e<sup>-θ<sup>τ</sup>x</sup>)

![](Images/Sigmoid%20function.png)

This function maps any real number to the range (0, 1) so to get a discrete 0 or 1 classification we map the output of the hypothesis function, with a linear decision boundary, as follows:
h<sub>θ</sub>(x) >= 0.5 --> 1
h<sub>θ</sub>(x) < 0.5 --> 0

*J*(θ<sub>0</sub>, θ<sub>1</sub>) is the **cost function** (squared error cost function) that tells how much off we are with the generated hypothesis with the current θ parameters.
To get better hypothesis we have to minimize the value returned by this function by changing the θ parameters.
![](Images/Cost%20function.png)