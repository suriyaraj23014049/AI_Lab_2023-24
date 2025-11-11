# Ex.No: 13 Learning – Machine Learning  
### DATE: 31-10-2025                                                                          
### REGISTER NUMBER : 212223060115
### AIM: 
To write a program to train the classifier to predict whether a tsunami can occur or not.
###  Algorithm:
#### 1. Load Data

- Read the earthquake dataset into a data structure (e.g., DataFrame).

#### 2. Preprocess Data

- Separate features X and target y (tsunami).

- Handle missing values if any (optional).

#### 3. Split Dataset

- Divide data into training set and test set (e.g., 80% train, 20% test).

- Maintain class balance using stratification.

#### 4. Train Model

- Initialize a Random Forest Classifier.

- Fit the model on training data X_train and y_train.

#### 5. Make Predictions

- Use the trained model to predict y_pred on X_test.

#### 6. Evaluate Model

- Compute accuracy score.

- Generate classification report (precision, recall, F1-score).

- Compute confusion matrix.

#### 7. Analyze Data

- Plot correlation heatmap of features.

- Plot top important features according to the model.

- Plot distribution of earthquake magnitude.

- Visualize confusion matrix.

### Program:
``` 
# ----- Import Libraries -----
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.model_selection import train_test_split
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import accuracy_score, confusion_matrix, classification_report

# ----- Step 1: Load Dataset -----
df = pd.read_csv("earthquake_data_tsunami.csv")
print("✅ Data Loaded Successfully!\n")
print(df.head())

# ----- Step 2: Define Features and Target -----
X = df.drop(columns=['tsunami'])
y = df['tsunami']

# ----- Step 3: Split into Train & Test -----
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42, stratify=y
)

# ----- Step 4: Train Model -----
model = RandomForestClassifier(
    n_estimators=150, max_depth=10, random_state=42
)
model.fit(X_train, y_train)

# ----- Step 5: Predict & Evaluate -----
y_pred = model.predict(X_test)
acc = accuracy_score(y_test, y_pred)

print(f"\n🎯 Model Accuracy: {acc*100:.2f}%")
print("\nClassification Report:\n", classification_report(y_test, y_pred))

# ----- Step 6: 4 Graphs for Analysis -----

# 1️⃣ Correlation Heatmap
plt.figure(figsize=(10, 6))
sns.heatmap(df.corr(), cmap='coolwarm', annot=False)
plt.title("Correlation Heatmap of Earthquake Features")
plt.show()

# 2️⃣ Feature Importance
feat_imp = pd.Series(model.feature_importances_, index=X.columns).sort_values(ascending=False)
plt.figure(figsize=(10, 6))
sns.barplot(x=feat_imp[:10], y=feat_imp.index[:10])
plt.title("Top 10 Important Features for Tsunami Prediction")
plt.xlabel("Importance")
plt.ylabel("Feature")
plt.show()

# 3️⃣ Magnitude Distribution
plt.figure(figsize=(8, 5))
sns.histplot(df['magnitude'], bins=20, kde=True)
plt.title("Earthquake Magnitude Distribution")
plt.xlabel("Magnitude")
plt.ylabel("Count")
plt.show()

# 4️⃣ Confusion Matrix
cm = confusion_matrix(y_test, y_pred)
plt.figure(figsize=(6, 4))
sns.heatmap(cm, annot=True, fmt='d', cmap='Blues')
plt.title("Confusion Matrix")
plt.xlabel("Predicted")
plt.ylabel("Actual")
plt.show()

```

### Output:

<img width="609" height="277" alt="{03934D9B-B8E3-48D2-9813-E3B04BCC918B}" src="https://github.com/user-attachments/assets/c7b77f6d-963a-4c1d-a476-e4561a7d24bf" />
<img width="830" height="589" alt="image" src="https://github.com/user-attachments/assets/e2348b27-9271-4df3-acab-de497252568e" /> 
<img width="899" height="547" alt="image" src="https://github.com/user-attachments/assets/eb55d4f2-4abc-47a5-960c-cda7866c9096" /> 
<img width="695" height="470" alt="image" src="https://github.com/user-attachments/assets/c0282ed9-6e62-4771-b8d4-cafc7b078981" /> 
<img width="501" height="393" alt="image" src="https://github.com/user-attachments/assets/e9d91907-6256-41d8-9bb5-d693dfeff282" />


### Result:
Thus the system was trained successfully and the prediction was carried out.
