# 🚢 Titanic Survival Prediction using Logistic Regression & Random Forest (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1knuGovDLeWkdfLsRmd1K-evndgYLG3Pp#scrollTo=DQkuXaQ-3pL_)

यह प्रोजेक्ट **Titanic Dataset** पर आधारित है, जिसमें हमने यह predict किया है कि कौन से passengers के **बचने (Survive करने)** की संभावना थी।  
Model बनाने के लिए हमने **Logistic Regression** और **Random Forest Classifier** का उपयोग किया है, और tuning के लिए **RandomizedSearchCV** किया गया है।  
पूरा काम **Google Colab** पर किया गया है।

---

## 🎯 Project Objective

Predict whether a passenger survived or not based on features like:
- Age  
- Gender  
- Passenger Class (Pclass)  
- Siblings/Spouse count (SibSp)  
- Parents/Children count (Parch)  
- Fare and Embarkation point  

---

## 🧩 Tech Stack

| Category | Tools / Libraries |
|-----------|------------------|
| Environment | Google Colab |
| Language | Python |
| Data Handling | pandas, numpy |
| Visualization | matplotlib, seaborn |
| ML Algorithms | Logistic Regression, Random Forest |
| Model Tuning | RandomizedSearchCV |
| Metrics | Accuracy, Confusion Matrix, Classification Report |

---

## 📊 Workflow Summary

1. **Data Loading**  
   - Titanic dataset (`titanic.csv`) को pandas से load किया गया।

2. **Data Cleaning**  
   - Missing values को fill किया गया (`Age` = mean, `Embarked` = mode)  
   - Irrelevant columns हटाए गए: `Cabin`, `Name`, `Ticket`, `PassengerId`  
   - Duplicate records हटाए गए  

3. **Exploratory Data Analysis (EDA)**  
   - Histogram और Boxplots से data distribution देखा गया  
   - `countplot` और `heatmap` से relationships visualize किए गए  

4. **Feature Encoding & Scaling**  
   - `LabelEncoder` से `Sex` को encode किया गया  
   - `pd.get_dummies()` से `Embarked` और `Pclass` को one-hot encode किया गया  
   - `StandardScaler` से `Age` और `Fare` scale किए गए  

5. **Modeling**  
   - Baseline: Logistic Regression  
   - Advanced: Random Forest Classifier  
   - Tuning: RandomizedSearchCV (best parameters select करने के लिए)  

6. **Evaluation**  
   - Accuracy, Confusion Matrix, और Classification Report generate किए गए  

---

## 🧠 Final Model Results (Random Forest)

| Metric | Value |
|--------|--------|
| **Accuracy** | **0.849** |
| **Confusion Matrix** | [[95, 10], [17, 57]] |
| **Precision (Class 0)** | 0.85 |
| **Precision (Class 1)** | 0.85 |
| **Recall (Class 0)** | 0.90 |
| **Recall (Class 1)** | 0.77 |
| **F1-score (Weighted Avg)** | 0.85 |

**Summary:**  
Model ने लगभग **85% accuracy** achieve की है, जो Titanic dataset के लिए काफी अच्छा performance है।  

---

## ⚙️ How to Run

### 🟢 Run on Google Colab
1. नीचे दिए गए लिंक पर क्लिक करें और notebook खोलें:  
   [Open in Colab](https://colab.research.google.com/drive/1knuGovDLeWkdfLsRmd1K-evndgYLG3Pp#scrollTo=DQkuXaQ-3pL_)  
2. Runtime connect करें  
3. Dataset (`titanic.csv`) upload करें  
4. सभी cells sequentially run करें  

### 💻 Local Run (Optional)
```bash
git clone https://github.com/Vikas8719/My-first-model.git
cd My-first-model
pip install -r requirements.txt
jupyter notebook firstproject_titanic.ipynb
