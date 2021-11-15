# sklearn-serving-demo



## Dependencies

Flask==1.0.2
numpy==1.16.3
pandas==0.24.2
scikit-learn==0.20.3

## Test the app


## Run the app
```
python main.py 8080

```


### Running API
```
python main.py <port>
```

# Endpoints
### /predict (POST)
Returns an array of predictions given a JSON object representing independent variables. Here's a sample input:
```
[
    {"Age": 85, "Sex": "male", "Embarked": "S"},
    {"Age": 24, "Sex": "female", "Embarked": "C"},
    {"Age": 3, "Sex": "male", "Embarked": "C"},
    {"Age": 21, "Sex": "male", "Embarked": "S"}
]
```

and sample output:
```
{"prediction": [0, 1, 1, 0]}
```


### /train (GET)
Trains the model. This is currently hard-coded to be a random forest model that is run on a subset of columns of the titanic dataset.

### /wipe (GET)
Removes the trained model.

