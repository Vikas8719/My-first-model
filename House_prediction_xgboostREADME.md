# House Price Prediction using XGBoost & Optuna (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Vikas8719/My-first-model/blob/main/Houseprices_prediction.ipynb)

This project predicts **house prices** using a full ML pipeline including EDA, data cleaning, feature engineering, model building with **XGBoost**, and hyperparameter tuning using **Optuna**, all implemented in **Google Colab**.

---

## 📂 Repository & Notebook Links

- GitHub Repository: https://github.com/Vikas8719/My-first-model  
- Colab Notebook: https://colab.research.google.com/github/Vikas8719/My-first-model/blob/main/Houseprices_prediction.ipynb  

---

## 🧩 Tech Stack & Tools

| Component | Technology / Library |
|----------|-----------------------|
| Environment | Google Colab |
| Language | Python |
| Data Handling | pandas, numpy |
| Visualization | matplotlib, seaborn |
| Machine Learning | scikit-learn, XGBoost |
| Hyperparameter Tuning | Optuna |

---

## 📊 Project Workflow

1. **Data Loading**  
   - Load dataset (CSV) in Colab or via Google Drive mount  

2. **Data Cleaning & Preprocessing**  
   - Handle missing values, outliers  
   - Encode categorical variables  
   - Scaling / normalization  

3. **Exploratory Data Analysis (EDA)**  
   - Plot distributions, correlations, boxplots etc.  

4. **Feature Engineering**  
   - Create new features, drop weak ones  

5. **Modeling**  
   - Baseline models (optional)  
   - Final model with **XGBoost**  

6. **Hyperparameter Tuning with Optuna**  
   - Search for best params  
   - Use cross-validation  

7. **Model Evaluation**  
   - Compute R², RMSE, MAE  
   - Visualize predictions vs actual  
Final XGBoost Model Performance:
RMSE: 29203.673298943086
R² Score: 0.5689942095377363

---

## ⚙️ How to Run / Reproduce

1. Click **“Open In Colab”** badge above (or use the Colab link).  
2. Connect to a runtime in Colab.  
3. Upload your dataset (if not already in repo) or mount Google Drive.  
4. Run all cells in the notebook.  

(Optional) If you want to run locally:

```bash
git clone https://github.com/Vikas8719/My-first-model.git
cd My-first-model
pip install -r requirements.txt
jupyter notebook Houseprices_prediction.ipynb
