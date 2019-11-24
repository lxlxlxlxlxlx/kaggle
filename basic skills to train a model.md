***
## Basic data exploration
```python3
### read file
import pandas as pd
train_data = pd.read_csv('XX.csv')

### show first 5 rows
train_data.head()

### show all columns' names and find the right prediction column
train_data.column
y = __

# show basic data 
train_data.describe()

# meaure the model with MAE
from sklearn.metrics import mean_absolute_error
mean_absolute_error(y,prediction)

# split the training data into two part: train and test

from sklearn.model_selection import train_test_split
train_X, val_X, train_y, val_y = train_test_split(X,y,random_state=0)
# random_state make sure we get same result every time we run this script

# adjust the parameters with trails
def get_mae(max_leaf_nodes, train_X, val_X, train_y, val_y):
    model = DecisionTreeRegressor(max_leaf_nodes=max_leaf_nodes, random_state=0)
    model.fit(train_X, train_y)
    preds_val = model.predict(val_X)
    mae = mean_absolute_error(val_y, preds_val)
    return(mae)
    
# after find the best parameters we train the model with whole data 

```
![google](https://www.kaggle.com/static/images/site-logo.png "google png")
