# Gradent Descent Coding Challenge
Written by Daniel Huang.

The code is for the Coding Challenge posted by Siraj on Youtube. (Intro to Math Intelligence)

# Objective
Find the best line fit of two variable using self-coded Gradient Descent.

# Dataset
The dataset I chose from Kaggle is the [Human Resources Analytics](https://www.kaggle.com/ludobenistant/hr-analytics).

The two variables I am interesting are the Average working hour per month and the satisfactory level of the employees.

# Overview
Note: the plots below has 

x-axis : Average working hour per month

y-axis : Satisfactory Level 
#### Sample Data scatter plot:
b=0 and m=0: 0.4373780052

![Alt text](/Gradient_Descent_Coding_Challenge/images/graph1.1.png "Optional Title")

#### After gradient descent

Error Value: 0.0845320879693

##### Plot:
![Alt text](/Gradient_Descent_Coding_Challenge/images/graph1.2.png "Optional Title")

##### Sample plot
b=1 and m=-0.001: 0.0984485869725

![Alt text](/Gradient_Descent_Coding_Challenge/images/graph2.1.png "Optional Title")

#### After gradient descent

Error value: 0.0694402235026
##### Plot
![Alt text](/Gradient_Descent_Coding_Challenge/images/graph2.2.png "Optional Title")

# Comments
### Vecotrized Gradient Descent
Initially I compute the MSE and gradient using for loop. However, the time was slow (about 22 sec to run 1000 iteration).

After modifying the code to using vectorized operation, the time to run was less than a second! 
### Learning rate and Nan issue
When first running gradient descent on this dataset, I encountered weight and bias to be Nan. 

After researching and trying different parameters, the solution was to lower the learning rate to prevent weight and bias to overflow in float32. 
### Interpretation of plots
The resulting plot with initialized weight and bias of 0 was not intuitive to me since it's indicating that employees are more satisfactory with higher avg working hours. 

I re-initialized the weight and bias to have negative slope. The error rate after running gradient descent is lower than the first attempt, which makes more sense. 

The reason that gradient descent did not result in lowest error rate may be due to the local minima and weight/bias initialization. 

# Credits
Big thanks to the great video and explanation by Siraj Raval and code examples by Matt Nedrich. 

