# 🚢 Titanic Survival Prediction using Decision Tree Classifier

[![Open In Colab](https://colab.research.google.com/drive/1knuGovDLeWkdfLsRmd1K-evndgYLG3Pp#scrollTo=DQkuXaQ-3pL_)](https://colab.research.google.com/drive/1knuGovDLeWkdfLsRmd1K-evndgYLG3Pp#scrollTo=DQkuXaQ-3pL_)

यह प्रोजेक्ट **Titanic Dataset** पर आधारित है, जिसमें यह predict किया गया है कि कौन से passengers के **survive करने की संभावना** थी।  
Model के लिए हमने **Decision Tree Classifier** का इस्तेमाल किया है और इसके hyperparameters को **RandomizedSearchCV** से optimize किया गया है।  
पूरा काम **Google Colab** पर किया गया है।

---

## 🎯 Objective

To build a machine learning model that can predict the survival of passengers aboard the Titanic ship based on their personal and travel information.

---

## 🧠 Tech Stack

| Category | Tools / Libraries |
|-----------|------------------|
| Environment | Google Colab |
| Language | Python |
| Data Handling | pandas, numpy |
| Visualization | matplotlib, seaborn |
| ML Algorithm | DecisionTreeClassifier |
| Optimization | RandomizedSearchCV |
| Metrics | Accuracy, Confusion Matrix, Classification Report |

---

## 📂 Dataset Information

**Dataset:** `titanic.csv`  
**Target Column:** `Survived` (1 = Survived, 0 = Not Survived)

**Important Features:**
- `Pclass` (Passenger Class)
- `Sex`
- `Age`
- `SibSp` (Siblings/Spouse)
- `Parch` (Parents/Children)
- `Fare`
- `Embarked`

---

## ⚙️ Data Preprocessing Steps

1. **Data Cleaning**
   - Removed unnecessary columns: `PassengerId`, `Name`, `Ticket`, `Cabin`
   - Filled missing values:
     - `Age` → Mean
     - `Embarked` → Mode
   - Dropped duplicate records

2. **Encoding & Scaling**
   - `LabelEncoder` for `Sex`
   - `OneHotEncoding` for `Embarked` and `Pclass`
   - `StandardScaler` for `Age` and `Fare`

3. **Train-Test Split**
   - 80% training, 20% testing (random_state = 42)

---

## 📊 Exploratory Data Analysis (EDA)

- Distribution plots using `sns.histplot()`
- Boxplots to identify outliers  
- Countplots for categorical columns  
- Heatmap for correlation between features  

---

## 🌲 Model Training

**Algorithm:** `DecisionTreeClassifier`  
**Hyperparameter Tuning:** `RandomizedSearchCV`  
**Parameters Tested:**
- `max_depth`
- `min_samples_split`
- `min_samples_leaf`
- `max_features`

**Best Parameters (Example):**
```python
{
 'max_depth': 20,
 'min_samples_split': 20,
 'min_samples_leaf': 2,
 'max_features': None
}
