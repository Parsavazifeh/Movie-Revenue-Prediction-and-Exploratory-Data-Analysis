
# 🎬 Movie Revenue Prediction

This project aims to **predict the box office revenue** of movies using their features and metadata. Since the actual revenue is calculated as:

```
revenue = box_office - budget
```

The core objective is to **predict the box office** value as precisely as possible based on the available features.

---

## 📌 Objectives

1. **Preprocess the dataset**: Clean and prepare the raw data for modeling.
2. **Explore and engineer features**: Select meaningful attributes and create new ones based on insights.
3. **Build and train prediction models**: Train multiple models and evaluate their performance.
4. **Analyze and interpret results**: Use visualizations and metrics to understand model behavior and determine the best-performing one.

---

## 🧰 Tools and Libraries

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost

Additional utilities and visual libraries may also be used during experimentation.

---

## 🧹 Data Preprocessing

Steps include:

- Removing or imputing missing values
- Parsing nested JSON-like fields (e.g., cast, crew, production companies)
- Converting date fields
- Handling categorical variables (e.g., genres, languages)
- Removing outliers or invalid entries

---

## 🔍 Feature Engineering

Key focus was on creating **new features that affect box office success**, such as:

- Number of top cast members
- Popularity score
- Director reputation (derived from past movie performance)
- Genre combinations
- Runtime categories
- Seasonal release date indicators (e.g., summer releases)

Only the most informative features were retained for modeling, while irrelevant ones were dropped.

---

## 🧠 Modeling Approach

Several machine learning models were trained and evaluated:

- **Linear Regression**
- **Random Forest Regressor**
- **Gradient Boosting**
- **XGBoost**

Model performance was assessed based on:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score

---

## 📊 Results & Evaluation

- Performance of each model was visualized using **residual plots**, **predicted vs actual** charts, and **error distributions**.
- The best-performing model was **XGBoost**, which captured non-linear patterns effectively.
- Justification: XGBoost performed well due to its ability to handle heterogeneous features and interactions, plus it is robust to overfitting when properly tuned.

---

## 📈 Final Model & Justification

The **XGBoost Regressor** with tuned hyperparameters (via Grid Search or manual tuning) provided the **lowest error** and **best generalization**. It was selected as the final model.

---

## 📁 Structure of Notebook

1. **Data Loading & Initial Inspection**
2. **Data Cleaning & Preprocessing**
3. **Exploratory Data Analysis**
4. **Feature Engineering**
5. **Model Training & Comparison**
6. **Final Model Evaluation**
7. **Conclusion and Takeaways**

---

## 📝 Notes

- Prediction accuracy alone is not the only goal; **interpretability and thoughtful feature creation** significantly influence scoring.
- Important insights were derived from **credit attributes** (cast, crew), which were crucial in crafting impactful features.
