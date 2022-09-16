## Problem Statement

Suppose you are starting a company that grows and sells wild mushrooms. 
- Since not all mushrooms are edible, you'd like to be able to tell whether a given mushroom is edible or poisonous based on it's physical attributes
- You have some existing data that you can use for this task.

  
## Dataset  
  
The collected dataset is as follows :  
  
| Cap Color | Stalk Shape | Solitary | Edible |
|:---------:|:-----------:|:--------:|:------:|
|   Brown   |   Tapering  |    Yes   |    1   |
|   Brown   |  Enlarging  |    Yes   |    1   |
|   Brown   |  Enlarging  |    No    |    0   |
|   Brown   |  Enlarging  |    No    |    0   |
|   Brown   |   Tapering  |    Yes   |    1   |
|    Red    |   Tapering  |    Yes   |    0   |
|    Red    |  Enlarging  |    No    |    0   |
|   Brown   |  Enlarging  |    Yes   |    1   |
|    Red    |   Tapering  |    No    |    1   |
|   Brown   |  Enlarging  |    No    |    0   |
  
  
-  We have 10 examples of mushrooms. For each example, we have
    - Three features
        - Cap Color (`Brown` or `Red`),
        - Stalk Shape (`Tapering` or `Enlarging`), and
        - Solitary (`Yes` or `No`)
    - Label
        - Edible (`1` indicating yes or `0` indicating poisonous)  
  
  
### 3.1 One hot encoded dataset
For ease of implementation, we have one-hot encoded the features (turned them into 0 or 1 valued features)

| Brown Cap | Tapering Stalk Shape | Solitary | Edible |
|:---------:|:--------------------:|:--------:|:------:|
|     1     |           1          |     1    |    1   |
|     1     |           0          |     1    |    1   |
|     1     |           0          |     0    |    0   |
|     1     |           0          |     0    |    0   |
|     1     |           1          |     1    |    1   |
|     0     |           1          |     1    |    0   |
|     0     |           0          |     0    |    0   |
|     1     |           0          |     1    |    1   |
|     0     |           1          |     0    |    1   |
|     1     |           0          |     0    |    0   |

Therefore,
- `X_train` contains three features for each example 
    - Brown Color (A value of `1` indicates "Brown" cap color and `0` indicates "Red" cap color)
    - Tapering Shape (A value of `1` indicates "Tapering Stalk Shape" and `0` indicates "Enlarging" stalk shape)
    - Solitary  (A value of `1` indicates "Yes" and `0` indicates "No")

- `y_train` is whether the mushroom is edible 
    - `y = 1` indicates edible
    - `y = 0` indicates poisonous
