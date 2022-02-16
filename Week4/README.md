[← Home](../README.md)

# Decision Trees

![example](https://user-images.githubusercontent.com/19282069/154310281-8a151a35-caee-4d73-abe9-8a520b13b192.png)

## Learning
![from-input](https://user-images.githubusercontent.com/19282069/154310446-1c1dd064-8044-479d-8669-0ec07213a3a0.png)

## Classification
ERROR = `nb of incorrect pred / total nb`
![classification](https://user-images.githubusercontent.com/19282069/154310528-27616f64-5d41-4491-95f3-babe6f174b92.png)

## Find the best tree
**GREEDY:**     
Approximately minimize the classification error on training data

![greedy](https://user-images.githubusercontent.com/19282069/154310957-c74d74b9-bb6a-4d64-819a-0b0eea4bb7a1.png)

### Which feature to split
Measuring effectiveness of split: ERROR rate from Classification above
![spit](https://user-images.githubusercontent.com/19282069/154311275-fdf877b0-4639-4f69-89be-ca68f03d57b4.png)

### When to stop
![leaf-node](https://user-images.githubusercontent.com/19282069/154311466-ac876453-ce78-4fa3-9ee6-74738035b4cc.png)

![final](https://user-images.githubusercontent.com/19282069/154311627-15694e5a-c8a3-4408-910a-8fe20e707116.png)

## Features with real values
- Age too random (0 to ~100)
- We use **Threshold split**
    - < 20 years
    - >= 20 years

### Find the best splitting threshold
![bestsplit](https://user-images.githubusercontent.com/19282069/154312039-bad49e85-63f3-4917-a1d0-393825b6e4f1.png)

# Multiclass Classification
![multiclass](https://user-images.githubusercontent.com/19282069/154312211-73e5f77e-8be4-4b65-b4cd-481ebcc22895.png)

# Overfitting in decision trees
- Tree depth indicate model complexity: **overfitting**
- Need to implement **Early stopping**

### Python
- `max_depth`
- `min_samples_split`
- `min_samples_leaf`

# Ensemble methods
Combine the predictions of several base estimators (ex: Decision trees) to improve robustness over a single estimator

## Bagging
![bagging](https://user-images.githubusercontent.com/19282069/154313012-0853a89a-0ff2-4c17-98c9-e0bb2d7e55e2.png)

## Random Forest
Bagging but: 
- sub-sample size is the same as original sample size
- when splitting pick the best split among a random subset of features
![random-forest](https://user-images.githubusercontent.com/19282069/154313090-264200cb-3057-4c4c-9eed-8aec3229f7af.png)