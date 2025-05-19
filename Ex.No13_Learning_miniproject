# Ex.No: 13 Learning_miniproject 
### DATE:13.5.2025                                                                            
### REGISTER NUMBER :212222220044
### AIM: 
To write a program to train the classifier for Blood Donation service center.
###  Algorithm:
1.Import libraries
(pandas, sklearn, matplotlib, seaborn)

2.Load the dataset
Read transfusion.csv using pandas.

3.Rename columns
Set column names to Recency, Frequency, Monetary, Time, Donated.

4.Split data
Separate features (X) and target (y), then split into training and testing sets.

5.Train model
Use RandomForestClassifier and train it with the training data.

6.Make predictions
Predict on the test set.

7.Evaluate

 1 Print accuracy
 2  Show confusion matrix
 3  Display classification report (precision, recall, F1-score)

### Program:
```
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import accuracy_score, classification_report, confusion_matrix
import matplotlib.pyplot as plt
import seaborn as sns

df = pd.read_csv('/content/transfusion.csv')
df.columns = ['Recency', 'Frequency', 'Monetary', 'Time', 'Donated']
X = df.drop('Donated', axis=1)
y = df['Donated']
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42

train_size = len(X_train)
test_size = len(X_test)
print(f"Total samples: {len(df)}")
print(f"Training samples: {train_size}")
print(f"Testing samples: {test_size}")

model = RandomForestClassifier(n_estimators=100, random_state=42)
model.fit(X_train, y_train)
y_pred = model.predict(X_test)
accuracy = accuracy_score(y_test, y_pred)
print(f"Accuracy: {accuracy * 100:.2f}%")

cm = confusion_matrix(y_test, y_pred)
sns.heatmap(cm, annot=True, fmt='d', cmap='Blues')

plt.title('Confusion Matrix')
plt.xlabel('Predicted')
plt.ylabel('Actual')
plt.show()
print("\nClassification Report:")
print(classification_report(y_test, y_pred))
```


### Output:
![Screenshot 2025-05-13 102306 - Copy](https://github.com/user-attachments/assets/98deca84-a460-46e0-9379-a9686ecd1963)




### Result:
Thus the system was trained successfully and the prediction was carried out.
