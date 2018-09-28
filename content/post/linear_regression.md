---
title: "Linear Regression"
date: 2018-09-28T10:12:00-06:00
image: images/ruler.jpg
tags: [
    "linear algebra",
    "gradient descent"
]
categories: [
    "linear regression"
]
draft: false
---

When building a supervised machine learning solution you need to have a training set. Data in this set is denoted as a mapping from one or more features denoted by x1, x2,… and an output y. So think of a training set like the age of trees and their heights. The age is x and the height is y. If we added another feature, the altitude at which the tree is growing we'd have x1 = age, x2 = altitude. 

The resulting function is frequently referred to as h or the hypothesis function. h(x1,…xn) -> y. For simple linear regression we have 

![Formula for linear regression (rise over run)](/images/linearRegression/linear_regression_formula.png)

This may look familiar and that's because it is a rise over run formula. 

Given a bunch of values we need to come up with a good value for the thetas that minimizes the distance the line is from the training points.

![Distance to best fit line](/images/linearRegression/distance_to_line.png)

To do this we want to minimize the value for 

![Cost function formula](/images/linearRegression/cost_function.png)

This particular version is called the squared error function but in general it is called the cost function. In ancient times "cost" started with the letter J so it makes sense to refer to this as J (not really).

With a single feature it is straight forward to understand a linear function which would minimize the cost. But as we more to larger numbers of features then the formula becomes more complex and we can't just intuit it. 

# Gradient Descent

Think of the J function for various values of theta 1 and theta 2 as being a surface plot. In order to find the minimum of a function we need to take a walk from a random starting location in the hopes of finding a global minimum. 

![A 3D surface plot](/images/linearRegression/descent.png)

From the random starting location you take a step in the direction which appears to be the most downhill from where you are. In that new location you repeat that step. Eventually you'll end up at a low point where you cannot step in any direction which will take you downhill. This might be the global minimum or just a local minimum. There is no way to tell. So you pick another spot and do another walk and see if the minimum you arrive at is better or worse than the first one.

The size of the step you take is referred to as alpha denoted by α. A simple version of the equation is

![The descent formula](/images/linearRegression/steps.png)

# Selecting α

Choosing a good value for α (alpha) is important. If you select too small a step then it increases the amount of time you spend because your steps are small. However, if you select too large a size for α then you could overstep a minimum and end up with a lower quality answer.