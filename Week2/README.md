[← Home](../README.md)

# Linear Regression

Statistical model to predict relationship between independent and dependant variables.

```y = ax + b```
- `y` dependant variable (*output*)
- `x` independent variable (*input*)
- `(x(i), y(i))` training example
- a list of *training examples*: **training set**

## Goal
![trainingset](https://user-images.githubusercontent.com/19282069/154038433-30da1681-66a7-4676-ab44-ebcf960c2a96.png)

Predict real valued outputs by modeling how observations are **associated** with some features as we change values of theses features

ℹ️ Regression is bout learning about relation between `x` and `y`

# Simple Linear Regression

## Model
![model](https://user-images.githubusercontent.com/19282069/154272065-167dbe6e-5510-4533-b257-67331d876f1f.png)

𝑦 = Θ₀ + Θ₁𝑥 + ε

- Θ model param

## Model Evaluation
![evaluation](https://user-images.githubusercontent.com/19282069/154272651-ab7daa8d-c1a3-410d-8fc9-79c550e02fa2.png)

**Which line is the best fit?**

### Cost function
Evaluate *performance of our algorithm*    
#### Takes:
- model outputs
- actual outputs  
#### Ouput  
= **high number** if predictions differ from reality

**Best hypothesis**     
hΘ(x), the one that minimize the cost function
![hypothesis](https://user-images.githubusercontent.com/19282069/154273662-ea1038cf-7c44-45ba-9cc1-c8173bc5eaef.png)

### Loss function
same as cost function but for a single training input

### Sum of errors [loss func]
Sum of errors in each iteration
![sumoferrors](https://user-images.githubusercontent.com/19282069/154274099-3defe6e2-a931-4fe5-877b-d72e697e45b0.png)

#### Example
![3points](https://user-images.githubusercontent.com/19282069/154274539-2ca8562d-50e4-43b1-95be-adb6823c0f15.png)

Issue here is sum = 0, the algorithm will assume that it has converged and good.

### Sum of absolute errors [loss func]
![sumofabserrors](https://user-images.githubusercontent.com/19282069/154275015-23bf6793-9374-4ba0-ae78-a8d20e394c35.png)

### Sum of Squared Errors [loss func]
![sumofsqrderrors](https://user-images.githubusercontent.com/19282069/154276322-ff64b563-fb97-47dc-a6c0-dc4ed7a835b0.png)

### R Squared [loss func]
metric: "how much varies **(y)** by changing **(x)**
- independent of context
- Coefficient of Determination

![formularsqrd](https://user-images.githubusercontent.com/19282069/154286317-bc8a961d-e0aa-4d68-9bf8-55fbacb201d5.png)
- Close to 1: large variability explained by regression
- Close to 0: regression did not explained

## Model Optimization
Find the best line automatically

### Gradient Descent
Optimization algorithm used to minimize some function by iteratively moving in the direct of steepest descent as defined by the negative of the gradient
![gradientdescent](https://user-images.githubusercontent.com/19282069/154290326-667d5441-5b26-4545-afb0-4e4b7f94758b.png)

**α** is the learning rate / step size
- *too small*: baby steps -> too long to converge
- *too large*: can overshoot -> fail to converge

#### Simple linear regression with GD
- Repeat until convergence
- Convergence means:
    - cost function is no longer changing
    - the numer of iterations is reached

# Multivariate Linear Regression
- Multiple features X=(x1,x2,...,xn)
- hΘ(𝑥) = Θ₀ + Θ₁𝑥₁ + Θ₂𝑥₂ + Θₙ𝑥ₙ

![multivariate](https://user-images.githubusercontent.com/19282069/154292646-aaa2dd3d-6dd9-4efe-8d6b-ded6c660e1a3.png)

# Assesing Performance
- Generalize unseen data
- Most used method: split data in train/test sets
![traintest](https://user-images.githubusercontent.com/19282069/154294056-9a9f2bc2-d5f7-4000-94c3-7aef54ca30b7.png)
- Learn Θ from training data

## Bias - Variance tradeoff
![variance](https://user-images.githubusercontent.com/19282069/154294250-63495931-a810-4a85-93de-70d523f999fb.png)

# Regularization
- Finding balance:
    - how well the model fits the data
    - magnitude of coefficients

By **incorporating a penalty** on weights Θ in the cost function.

![ridge-lasso](https://user-images.githubusercontent.com/19282069/154297877-c97f87fe-baa6-4f9a-af37-03c77208f1c8.png)