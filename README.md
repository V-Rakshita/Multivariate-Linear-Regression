# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
Import pandas for data manipulation and linear_model from sklearn for regression.

### Step2
 Load the CSV file carsemission.csv into a DataFrame using pd.read_csv.

### Step3
Define X as a DataFrame containing the Weight and Volume columns. Define y as the CO2 column, which is the value to predict.

### Step4
Create a linear regression model instance using linear_model.LinearRegression(). Train the model with the data by calling regr.fit(X, y).

### Step5
Access model coefficients with regr.coef_, showing the weight of each feature. Access the intercept term with regr.intercept_, representing the baseline CO2.

### Step6
Create a DataFrame input_data with new values for Weight and Volume. Use regr.predict(input_data) to predict CO2 for the input features.

### Step7
End the program

## Program:
```python
import pandas as pd
from sklearn import linear_model
df = pd.read_csv("carsemission.csv")
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:', regr.intercept_)
input_data = pd.DataFrame({'Weight': [3300], 'Volume': [1300]})
predictedCO2 = regr.predict(input_data)
print('Predicted CO2 for the corresponding weight and volume:', predictedCO2)
```
## Output:

### Insert your output

![MULTIVARIATE](https://github.com/user-attachments/assets/a0336ad2-469e-4967-af12-4264b87cec56)
<br>

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
