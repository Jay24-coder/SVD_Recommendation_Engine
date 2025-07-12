# 🎬 MovieLens Recommendation System

This project demonstrates how to build a movie recommendation system using the [MovieLens](https://grouplens.org/datasets/movielens/) dataset and the Singular Value Decomposition (SVD) algorithm from the `surprise` library. The system predicts movie ratings for a given user and recommends top-rated movies that the user has not seen yet.

---

## 📂 Dataset Information

The project uses the following two datasets from the `movielens` folder:

### `ratings.csv`
- Shape: **1,048,575 rows × 4 columns**
- Columns:
  - `userId`: ID of the user
  - `movieId`: ID of the movie
  - `rating`: Rating given by the user (0.5 to 5.0)
  - `timestamp`: Time of rating (not used in modeling)

### `movies.csv`
- Shape: **27,278 rows × 3 columns**
- Columns:
  - `movieId`: ID of the movie
  - `title`: Movie title
  - `genres`: Pipe-separated genres associated with the movie

---

## 🧠 Model: SVD (Singular Value Decomposition)

The recommendation model is built using the SVD algorithm provided by the `surprise` library.

### Steps:
1. **Data Loading & Exploration**: Load and examine ratings and movies datasets.
2. **Matrix Creation**: Pivot the ratings data into a user–movie matrix.
3. **Model Training**: Use `surprise.SVD` with cross-validation (RMSE and MAE metrics).
4. **Prediction for a User**: Predict ratings for all movies for user `userId = 1`.
5. **Recommendation Generation**: Recommend top-rated movies that the user hasn’t rated yet.

---

## 🔍 Example Output

### ✅ Movies Rated 5 by User 1:
Display of movies that user 1 has rated with a 5.

### ⭐ Recommendations:
Top predicted movies for user 1 based on the SVD model, sorted by estimated score (highest to lowest).

---

## 📦 Libraries Used

- `pandas`
- `numpy`
- `scikit-surprise`
  - `Reader`, `Dataset`, `SVD`
  - `cross_validate`

---

## 📁 Folder Structure

movielens/
├── ratings.csv
├── movies.csv
├── recommendation_system.py
└── README.md