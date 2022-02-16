[← Home](../README.md)

# Context

## Classification problem
![binary](https://user-images.githubusercontent.com/19282069/154302845-fefad876-6f72-4889-81b5-e54dedc90aa7.png)
![multi](https://user-images.githubusercontent.com/19282069/154302781-dbfb4a07-071b-401c-90b8-9b71c16cb72c.png)

### Can linear regression help ?
1. Linear Regression can sometimes be lucky
2. Classification need categorical values
    - y = 0 or 1 when LR can be > 1 or < 0
3. We need to know how confident our prediction is

# Logistic Regression
## Model
![model](https://user-images.githubusercontent.com/19282069/154303314-fd154ebc-9035-4859-b525-09932562a1ce.png)
![interpretation](https://user-images.githubusercontent.com/19282069/154303421-2bfef2b0-e773-496b-958a-2be4f288332d.png)

## Decision boundary
Decision regions separated by **decision boundaries**

![boundaries](https://user-images.githubusercontent.com/19282069/154303588-04ac0fd9-5898-4ab1-9986-c12a27895171.png)

# Multicass classification
![onevsall](https://user-images.githubusercontent.com/19282069/154304379-03c58304-4ad2-4340-ab04-b33d8567350c.png)

# Evaluating classifiers
![cancer](https://user-images.githubusercontent.com/19282069/154305025-1443da29-18d7-42cd-afeb-bc52f75c528a.png)
## Confusion matrix
![confusionmatrix](https://user-images.githubusercontent.com/19282069/154305339-564839a2-8af6-4397-87e3-f447aa66be05.png)

## Accuracy
= number of data points classified correctly / all data points

`= (TP+TN)/(FP+FN+TP+TN)`

Error of classification = `1-Accuracy = (FP+FN)/(FP+FN+TP+TN)`

### Precision
= True positive / (True positive + False positive)

### Recall
= True positive / (True positive + False negative)

# K-fold cross-validation
Data = Training set + Testing set
- Each data point is used only once for training or for testing
-  Moreover: Sometimes we do not have enough data available to make reliable partitions

![kfold](https://user-images.githubusercontent.com/19282069/154305984-ac879f2f-f359-44ef-9d1a-5e2e1f755279.png)

- Robust for parameter tuning
- Multiple rounds with averaged results