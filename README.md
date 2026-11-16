# Rotten Tomatoes Audience Score Prediction

Predicting whether audiences will like a movie from **critics' reviews and movie metadata**, using the [Clapper – Massive Rotten Tomatoes Movies & Reviews](https://www.kaggle.com/datasets/andrezaza/clapper-massive-rotten-tomatoes-movies-and-reviews) dataset.

## Approach

- **Cleaning** – dropping sparse and high-cardinality columns (writer, director, …) and redundant fields; merging the reviews and movies tables per movie.
- **Text features** – each critic review is scored with sentiment analysis (NLTK VADER / TextBlob, −1 … 1) and aggregated into a per-movie *critic positivity* feature.
- **Engineered features** – normalized critic score, tomatometer, runtime and release date; one-hot genres (top 5) and ratings; a *top-critic ratio* feature.
- **Models** – k-Nearest Neighbors and Logistic Regression, compared for classifying audience reception.

## Tech stack

pandas · scikit-learn · NLTK · TextBlob · Matplotlib / Seaborn

## Running

Download the dataset from Kaggle (link above), place the CSV files next to the notebook and run `dataScienceProje.ipynb`.

---
Developed for a data science course at Hacettepe University, Department of Artificial Intelligence Engineering.
