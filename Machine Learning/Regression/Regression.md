A regression algorithm can generate a value, a float, based on the input data.
This algorithm is trained by giving some data as input and it returns a float as output. (Example hose price prediction based on size)

Regression uses **Supervised Learning** as training algorithm to predict a **target** (output) starting from one or more **features** (input)

*m* = Number of training Examples
x<sub>1</sub>,x<sub>2</sub>...x<sub>n</sub> = Features
y<sub>1</sub>,y<sub>2</sub>...y<sub>n</sub> = Target
(x, y) = One training example
(x<sup>(i)</sup>,y<sup>(i)</sup>) = i-th training example (one row of the table)

| Size in Feet<sup>2</sup>    | Price in $K              |
| --------------------------- | ------------------------ |
| 2104<br>1416<br>1534<br>852 | 460<br>232<br>315<br>178 |
![](Images/1.png)
*h* = Hypothesis


## Linear Regression
The house example is a linear regression with one variable:
	h<sub>θ</sub>(x<sub>1</sub>) = θ<sub>0</sub> + θ<sub>1</sub>x<sub>1</sub>
we can represent this with two vectors:
θ = \[ θ<sub>0</sub> θ<sub>1</sub> \]            x = \[ 1 x<sub>1</sub> \]

The vector θ contains the parameters, which are the values that then will help generating the hypothesis based on the features. The base idea is to find a vector so that h<sub>θ</sub>(x) is the closest to the training examples (x, y)

![](Images/Cost%20Function.png)

*J*(θ<sub>0</sub>, θ<sub>1</sub>) is the **cost function** (squared error cost function) that tells how much off we are with the generated hypothesis with the current θ parameters.
To get better hypothesis we have to minimize the value returned by this function by changing the θ parameters.
If we plot this cost function on a 3D graph it will be looking something like this.

![](Images/Cost%20function%203D%20Graph.png)

If we transform the 3D graph into a 2D one (Contour Plot)
![](Images/Cost%20function%202D%20Graph.png)

#### Gradient Descent
Gradient Descent is an algorithm to minimize a function without calculating all possible values of the function by moving step by step in a valley.

![](Images/Gradient%20Descent%20Genereal%20Idea.png)

