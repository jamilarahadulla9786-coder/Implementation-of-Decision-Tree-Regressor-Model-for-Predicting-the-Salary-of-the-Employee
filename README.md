# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the required libraries such as NumPy, Pandas, and Scikit-learn. 
2. Load the dataset containing employee position levels and salaries.
3. Create a Decision Tree Regressor model.Fit the model using the training data.
4. Visualize the results using a graph for better understanding.

## Program:
```
/*
# Import required libraries
import pandas as pd
import numpy as np
from sklearn.tree import DecisionTreeRegressor, plot_tree
from sklearn.model_selection import train_test_split
from sklearn.metrics import mean_absolute_error, mean_squared_error, r2_score
import matplotlib.pyplot as plt

# Step 1: Load dataset
df = pd.read_csv("Salary.csv")

print("Dataset Preview:")
print(df.head())

# Step 2: Select features and target
# Change column names if your CSV has different names
X = df[["Level"]]   # Independent variable
y = df["Salary"]              # Dependent variable

# Step 3: Train-Test Split
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.3, random_state=42
)

# Step 4: Create Decision Tree Regressor
model = DecisionTreeRegressor(
    criterion="squared_error",
    max_depth=3,
    random_state=42
)

# Step 5: Train the model
model.fit(X_train, y_train)

# Step 6: Make predictions
y_pred = model.predict(X_test)

# Step 7: Evaluate the model
mse = mean_squared_error(y_test, y_pred)
rmse = np.sqrt(mse)

print("MAE  :", mean_absolute_error(y_test, y_pred))
print("MSE  :", mse)
print("RMSE :", rmse)
print("R2   :", r2_score(y_test, y_pred))

# Step 8: Plot Decision Tree
plt.figure(figsize=(16, 10))
plot_tree(
    model,
    feature_names=["Level"],
    filled=True
)
plt.title("Decision Tree Regressor for Employee Salary Prediction")
plt.show()

# Step 9: Predict salary for new employee
new_exp = [[5]]  # 5 years experience
predicted_salary = model.predict(new_exp)
print("\nPredicted Salary for 5 years experience:", predicted_salary[0])
```
Developed by: ABDUL RAHMAN A R
RegisterNumber:  25008775


## Output:
![Decision Tree Regressor Model for Predicting the Salary of the Employee](sam.png)
![9 1](https://github.com/user-attachments/assets/186fae9a-c3ea-4a9c-90f6-e054c886cf1a)
![9 2](https://github.com/user-attachments/assets/b258808c-8f96-4ee8-9801-4a5bc2529b1f)
![9 3](https://github.com/user-attachments/assets/7a8d82df-5263-44c6-bd69-c5fd533aac8f)


## Result:
Thus the program to 
implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
