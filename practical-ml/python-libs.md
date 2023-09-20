# pandas

```py
import pandas as pd

some_file_path = '../path-to-file'
my_data = pd.read_csv(some_file_path)

 # summarize data
my_data.describe()

# get columns
my_data.columns 

# dropna drops missing values (na = "not available")
my_data = my_data.dropna(axis=0)

# show top rows
my_data.head()
```

# scikit-learn

Example defining a model and fitting it w/ features and target variable:
```py
from sklearn.tree import DecisionTreeRegressor

# Define model. Specify a number for random_state to ensure same results each run
my_model = DecisionTreeRegressor(random_state=1)

# Fit model
my_model.fit(X, y)
```

## Calculating MAE

```py
from sklearn.metrics import mean_absolute_error

predicted_prices = my_model.predict(X)
mean_absolute_error(y, predicted_prices)
```

## Splitting data randomly

```py
rain_X, val_X, train_y, val_y = train_test_split(X, y, random_state = 0)
# Define model
my_model = DecisionTreeRegressor()
# Fit model
my_model.fit(train_X, train_y)

# get predicted prices on validation data
val_predictions = my_model.predict(val_X)
print(mean_absolute_error(val_y, val_predictions))
```

`max_leaf_nodes` is a utility func that can be used to control tree depth.

eg. 
```py
my_model = DecisionTreeRegressor(max_leaf_nodes=max_leaf_nodes, random_state=0)
```

# use random forests model
```py
from sklearn.ensemble import RandomForestRegressor
from sklearn.metrics import mean_absolute_error

my_model = RandomForestRegressor(random_state=1)
my_model.fit(train_X, train_y)
pred_results = my_model.predict(val_X)
print(mean_absolute_error(val_y, pred_results))
```