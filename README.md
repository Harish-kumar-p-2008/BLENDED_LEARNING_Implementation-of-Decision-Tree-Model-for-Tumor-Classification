# BLENDED_LEARNING
# Implementation of Decision Tree Model for Tumor Classification

## AIM:
To implement and evaluate a Decision Tree model to classify tumors as benign or malignant using a dataset of lab test results.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import Libraries: Bring in the required libraries such as NumPy, Pandas, Scikit-learn, and Matplotlib.
2. Load the Dataset: Load the tumor classification dataset containing medical features such as tumor size, texture, radius, and other related attributes.
3. Data Preprocessing: Check for missing values, clean the dataset if necessary, and encode categorical variables if present.
4. Define Features and Target: Separate the dataset into features (X) representing tumor characteristics and the target variable (y) representing the tumor class (Benign or Malignant).
5. Split Data: Divide the dataset into training data and testing data using the train-test split method.
6. Build Decision Tree Model: Initialize the Decision Tree Classifier with suitable parameters such as criterion (gini or entropy).
7. Train the Model: Fit the Decision Tree model using the training dataset to learn the patterns for tumor classification.
8. Evaluate Performance: Evaluate the model using performance metrics such as accuracy score, confusion matrix, and classification report.
9. Visualize the Decision Tree: Display the structure of the decision tree to understand how the model makes classification decisions.
10. Make Predictions & Compare: Use the trained model to predict tumor classes for the test dataset and compare the predicted results with the actual values.
## Program:
```
/*
Program to  implement a Decision Tree model for tumor classification.
Developed by: Harish Kumar P
RegisterNumber:  25006070

import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeClassifier
from sklearn.metrics import accuracy_score, classification_report, confusion_matrix
import seaborn as sns
import matplotlib.pyplot as plt

data = pd.read_csv('tumor.csv')
print(data.head())
print(data.columns)

print(data.columns)
X = data.drop(columns=['Class']) 
y = data['Class']
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3, random_state=42)
model = DecisionTreeClassifier(random_state=42)
model.fit(X_train, y_train)

y_pred = model.predict(X_test)
accuracy = accuracy_score(y_test, y_pred)
print("Name: Harish Kumar P")
print("Register Number: 25006070")
print("Accuracy:", accuracy)
print("Classification Report:\n", classification_report(y_test, y_pred))
conf_matrix = confusion_matrix(y_test, y_pred)
sns.heatmap(conf_matrix, annot=True, fmt="d", cmap="Blues")
plt.xlabel("Predicted")
plt.ylabel("Actual")
plt.title("Confusion Matrix")
plt.show()
*/
```

## Output:
![alt text](<Screenshot 2026-03-12 155038.png>)
![alt text](<Screenshot 2026-03-12 155049.png>)
![alt text](<Screenshot 2026-03-12 155058.png>)
![alt text](<Screenshot 2026-03-12 155104.png>)
## Result:
Thus, the Decision Tree model was successfully implemented to classify tumors as benign or malignant, and the model’s performance was evaluated.
