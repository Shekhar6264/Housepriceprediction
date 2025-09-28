# House Price Prediction

Predict house sale prices using machine learning on the Ames Housing dataset.

---

## **Overview**
This project predicts house prices based on features like square footage, number of bathrooms, age, and neighborhood. The workflow includes:

- Data preprocessing & missing value handling
- Feature engineering
- Model training (Linear Regression, XGBoost)
- Evaluation (RMSE, MAE, R²)
- Generating predictions for submission

---

## **Dataset**
- `train.csv` → features + `SalePrice`
- `test.csv` → features for prediction

---

## **Key Steps**
1. Log-transform target variable to reduce skewness.
2. Impute missing values (median, mode, or 0/None as appropriate).
3. Create new features: `TotalSF`, `TotalBath`, `Age`.
4. Encode categorical features with one-hot encoding.
5. Scale features for Linear Regression; XGBoost works without scaling.

---

## **Modeling**
- **Linear Regression**  
- **XGBoost Regressor** with tuned hyperparameters:
  - `n_estimators=1000`, `learning_rate=0.05`, `max_depth=3`, `subsample=0.8`, `colsample_bytree=0.8`

---

## **Usage**
1. Install dependencies:
```bash
pip install -r requirements.txt
