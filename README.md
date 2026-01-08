# Linear Regression without external CSV

import pandas as pd
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression

# Step 1: Create data directly in the script
data = {
    "years_of_experience": [1, 2, 3, 4, 5, 6, 7, 8, 9, 10],
    "salary": [45000, 50000, 60000, 80000, 110000, 150000, 180000, 210000, 250000, 300000]
}

# Step 2: Convert to DataFrame
df = pd.DataFrame(data)

print("Data used for Linear Regression:")
print(df)

# Step 3: Prepare features and target
X = df[['years_of_experience']]  # 2D array
y = df['salary']                 # 1D array

# Step 4: Train Linear Regression model
model = LinearRegression()
model.fit(X, y)

# Step 5: Make predictions
y_pred = model.predict(X)

# Step 6: Plot actual vs predicted
plt.scatter(X, y, color='blue', label='Actual')
plt.plot(X, y_pred, color='red', label='Predicted')
plt.xlabel("Years of Experience")
plt.ylabel("Salary")
plt.title("Linear Regression: Experience vs Salary")
plt.legend()
plt.show()
# program-to-implement-linear-regression
linear regression: experience vs  salary
