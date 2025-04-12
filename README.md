# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the standard libraries.

2. Upload the dataset and check for any null values using .isnull() function.

3. Import LabelEncoder and encode the dataset.

4. Import DecisionTreeRegressor from sklearn and apply the model on the dataset.

5. Predict the values of arrays.

6. Import metrics from sklearn and calculate the MSE and R2 of the model on the dataset.

7. Predict the values of array.

8. Apply to new unknown values.
## Program:
```python
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: KISHORE.S
RegisterNumber: 212224230130
*/
import pandas as pd
data = pd.read_csv("Salary.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
data["Position"] = le.fit_transform(data["Position"])
data.head()
x = data[["Position", "Level"]]
y = data["Salary"]
from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test = train_test_split(x, y, test_size=0.2)
from sklearn.tree import DecisionTreeRegressor
dt = DecisionTreeRegressor()
dt.fit(x_train, y_train)
y_pred = df.predict(x_test)
from sklearn import metrics
mse = metrics.mean_squared_error(y_test, y_pred)
mse
r2 = metrics.r2_score(y_test, y_pred)
r2
dt.predict([[5,6]])
```

## Output:
HEAD:

![Screenshot 2025-04-12 231607](https://github.com/user-attachments/assets/db3fb6c8-e851-4f16-98a5-506197d787ab)

INFO:

![Screenshot 2025-04-12 231615](https://github.com/user-attachments/assets/98d3f009-4acb-429d-919a-ddcc3f690721)

NULL VALUES:

![Screenshot 2025-04-12 231621](https://github.com/user-attachments/assets/f7463332-98fc-4ab0-a824-0964867bd58d)

ENCODED VALUES:

![Screenshot 2025-04-12 231628](https://github.com/user-attachments/assets/0c592b7d-752f-48cd-a936-eda65e05ffa3)

MSE:

![Screenshot 2025-04-12 231636](https://github.com/user-attachments/assets/e4e0975e-9b01-4ac6-83f1-32d28437a77d)

R2:

![Screenshot 2025-04-12 231644](https://github.com/user-attachments/assets/d9c22628-7e20-4349-a6d9-adb9d33c22c2)

PREDICTED VALUES:

![Screenshot 2025-04-12 231658](https://github.com/user-attachments/assets/4ad02b3b-f8fb-4700-bde7-3578035e5f35)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
