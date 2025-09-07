# 🏡 California Housing Price Prediction

## 📌 Project Overview
This project aims to build a machine learning model to **predict house prices in California** using the famous `housing.csv` dataset.  
We apply **feature engineering**, **data preprocessing**, and train two machine learning models:  
- **Linear Regression**  
- **Random Forest Regressor**

Finally, we evaluate both models to compare their performance.

---

## 📂 Dataset
- Source: `housing.csv`  
- Contains information about housing districts in California, including:  
  - `longitude`, `latitude` → geographical info  
  - `housing_median_age`, `total_rooms`, `total_bedrooms`, `population`, `households` → demographics & housing info  
  - `median_income` → average income per district  
  - `ocean_proximity` → categorical feature describing distance to ocean  
  - `median_house_value` → **Target (house price)**

---

## ⚙️ Data Preprocessing
1. **Handle missing values** in `total_bedrooms`.  
2. **Log transformation** on skewed features (`total_rooms`, `total_bedrooms`, `population`, `households`).  
3. **One-hot encoding** for categorical variable `ocean_proximity`.  
4. **Feature engineering**:  
   - `bedrooms_per_room = total_bedrooms / total_rooms`  
   - `household_rooms = total_rooms / households`  
5. **Scaling** numerical features with `StandardScaler`.

---

## 🧠 Models Used
### 1. Linear Regression
- A simple baseline model.  
- Fast but underfits the data.  

### 2. Random Forest Regressor
- An ensemble method based on decision trees.  
- Captures non-linear relationships.  
- Provides better accuracy on this dataset.  

---

## 📊 Results
- **Linear Regression** → Lower R² score (underfitting).  
- **Random Forest** → Better R² score and more reliable predictions.  

*(Exact metrics will depend on train/test split and parameters.)*

---
## 📌 Key Insights
- Housing prices are strongly correlated with **median income**.  
- **Random Forest** performs significantly better than Linear Regression for this dataset.  
- Feature engineering (e.g., `bedrooms_per_room`) improves prediction accuracy.  

---

## 📈 Future Improvements
- Hyperparameter tuning with `GridSearchCV`.  
- Try advanced models like **XGBoost** or **Gradient Boosting**.  
- Deploy model as a web app (e.g., **Flask**, **FastAPI**, or **Streamlit**).  

## 🚀 How to Run
1. Clone this repository and install dependencies:
   ```bash
   pip install -r requirements.txt
