# 🎬 Movie Ratings Classification Project

This project focuses on cleaning, exploring, and building classification models to predict the **rating category** of movies using metadata such as **genre**, **cast**, **duration**, and **votes**.

---

## 🧹 Data Cleaning and Preprocessing

Several cleaning steps were performed to ensure data quality and consistency:

- Converted the `Year` and `Duration` columns to numeric format after removing unwanted characters.
- Handled missing values:
  - Dropped rows with missing actor names or release years.
  - Filled missing `Votes` with the **median** value.
  - Filled missing `Rating` with the **mean** value.
  - Imputed missing `Duration` using the **genre-based mean**.
- Simplified the `Genre` column by keeping only the **primary genre**.

---

## 📊 Data Visualization & Insights

Visualizations were used to better understand relationships between variables and draw insights:

- Average duration by genre
- `Votes` vs `Rating` and `Duration` vs `Rating` (scatterplots)
- Rating distribution across genres
- Top 10 actors and directors by average rating and film count
- Number of movies released per year
- Trend of average rating over the years

**Insights:**
- Some genres consistently have higher or lower durations.
- `Votes` and `Ratings` are positively correlated.
- Certain actors and directors tend to appear more frequently or receive higher ratings.

---

## 🛠️ Feature Engineering

To prepare the data for modeling:

- Created a new column `Rating_Class` to classify movies:
  - **High**: rating ≥ 6
  - **Medium**: 5 ≤ rating < 6
  - **Low**: rating < 5
- Counted actor appearances:
  - `Actor 1_Count`, `Actor 2_Count`, `Actor 3_Count`
- Used **Label Encoding** for actors and directors.
- Applied **One-Hot Encoding** to the `Genre` column (e.g., `Genre_Action`, `Genre_Comedy`, etc.).
- Dropped unnecessary columns such as `Name`, raw `Genre`, and raw `Rating`.

---

## 🧰 Model Training and Evaluation

After preprocessing and feature engineering, machine learning models were trained to classify movies into rating categories.

### 🧪 Preprocessing:

- Data split using `train_test_split`
- Features scaled using `StandardScaler`

---

### 🌲 Model 1: Random Forest Classifier

- **Accuracy**: ~70%
- Strong at distinguishing **High** and **Low** rating classes.
- Confusion matrix revealed some confusion around the **Medium** category.

---

### ➕ Model 2: Logistic Regression

- Simpler model with **lower accuracy** than Random Forest.
- Misclassified many **Medium** and **Low** rated movies.

---

## 📌 Conclusion

- **Random Forest** outperformed Logistic Regression in classifying movie ratings.
- **Feature engineering** (like encoding and genre dummies) improved model accuracy.
- **Data visualizations** revealed important patterns and guided feature design.
- Future improvements:
  - Hyperparameter tuning
  - Exploring other models or ensemble methods to improve classification performance.
