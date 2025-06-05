# 🚗 Predictive Analysis of Car Prices

## 🔎 Objective

This project focuses on **predicting the Manufacturer’s Suggested Retail Price (MSRP)** of vehicles using machine learning techniques. Leveraging over 11,000 entries with diverse car features like engine size, fuel type, transmission, and body style, the goal is to understand which features most influence car pricing and develop accurate predictive models.

---

## 📦 Dataset Summary

- 🛠️ 11,000+ car records  
- 📊 16 features including make, model, year, engine, and fuel specs  
- 🎯 Target variable: `MSRP` (continuous)

---

## 🧼 Data Preparation Steps

- 🔍 Handled null values and removed duplicates  
- ❌ Dropped irrelevant feature `Market.category`  
- 🧠 Engineered new variable: `car_age = 2017 - year`  
- 🔄 Encoded categorical variables (e.g., Make, Fuel Type, Transmission)

---

## 📚 Modeling Approach

- **Train-Test Split**: 70% training, 30% testing using random sampling  
- **Models Used**:  
  - 🌲 Random Forest  
  - 🌿 Decision Tree  
  - 🚀 Gradient Boosting

---

## 📈 Evaluation Metrics

Each model was evaluated using:

- 🧮 **RMSE** (Root Mean Squared Error)  
- 📐 **R² Score**  
- 📊 **MAE** (Mean Absolute Error via bootstrapping)

| Model              | R² Score | RMSE     | Notes                            |
|-------------------|----------|----------|----------------------------------|
| Random Forest      | 0.845    | ~17,083  | Best overall performance         |
| Decision Tree      | 0.839    | ~27,116  | Simple and interpretable         |
| Gradient Boosting  | 0.705    | ~36,467  | Underperformed slightly          |

---

## 🔁 Bootstrapping Results (Random Forest)

- 📉 Avg. RMSE: 22,355  
- 🔁 Std. Dev (RMSE): 8,052  
- 📈 Avg. R²: 0.874

---

## 🧠 Key Insights

- 🚘 **Engine HP** and **Engine Cylinders** had the strongest correlation with MSRP  
- ⛽ Regular Unleaded was the most common fuel type  
- 🧪 ANOVA revealed statistically significant differences in MSRP based on:  
  - Make  
  - Fuel Type  
  - Transmission  
  - Vehicle Size & Style

---

## ✅ Conclusion

The **Random Forest model** performed best, effectively capturing the nonlinear relationships between features and car price. The model achieved high predictive accuracy and stability across bootstrap samples.

---

## 🔭 Future Work

- 🧠 Explore **neural networks** or hybrid ensembles for better accuracy  
- 🌐 Include external data such as fuel prices, market trends, or brand reputation  
- 🧩 Integrate model with a **real-time car pricing tool or API**

