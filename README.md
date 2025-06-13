# 🎬 Movie Rating Classification Project

This project classifies movies into three rating categories: **Low**, **Medium**, and **High** using a range of features including year, duration, votes, genre, actors, and director information.

## 💡 Goal

To build an efficient classification model that predicts movie rating levels using machine learning algorithms such as **Random Forest** and **Logistic Regression**.

---

## 🧹 Data Cleaning & Preprocessing

- Converted `Year` and `Duration` columns to numeric format and fixed inconsistencies.
- Removed missing values from key columns like `Year`, `Actor 1`, `Actor 2`, `Actor 3`.
- Replaced missing values in `Votes` and `Rating` with median and mean respectively.
- Extracted the primary genre from the `Genre` column.
- Handled missing durations by imputing with the mean duration per genre.

---

## 📊 Data Visualization

Visual insights were extracted using plots such as:

- Movie `Duration` by `Genre`
- `Rating` vs `Votes` and `Duration`
- Number of movies released per year
- Top 10 actors and directors by rating and film count
- Average rating trend over the years

These visualizations helped understand feature relationships and data distribution.

---

## 🛠️ Feature Engineering

- Created a new categorical feature `Rating_Class` based on numerical rating.
- Encoded categorical variables (`Actor 1`, `Actor 2`, `Actor 3`, `Director`) using Label Encoding.
- Counted the number of times each actor appeared in the dataset (`Actor 1_Count`, etc.).
- One-hot encoded the `Genre` column.
- Dropped unused columns like `Name`, `Genre`, and raw `Rating`.

---

## 🤖 Models Used

- **Random Forest Classifier**: Achieved ~70% accuracy.
- **Logistic Regression**: Also evaluated for comparison.

Both models were trained and tested, and evaluated using metrics like precision, recall, F1-score, and confusion matrix.

---

## 📂 Project Structure

