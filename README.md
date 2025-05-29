# SI370Project
# Spotify Song Popularity Analysis

This project explores what factors contribute to a song’s popularity on Spotify. Using two large datasets, we investigated how variables such as tempo, energy, release year, danceability, and acoustics relate to Spotify's popularity metric. We also experimented with a machine learning model to evaluate the potential for predicting song popularity.

## Exploratory Questions

We centered our analysis around the following questions:

1. How does tempo affect a song’s popularity across different genres?
2. Do songs with higher energy levels tend to have more streams?
3. Is there a correlation between release year and song popularity?
4. How do danceability and acoustics contribute to popularity?

## Datasets

We used two complementary datasets to ensure robust results and reduce bias:

**Dataset 1: Spotify Songs Dataset**  
- Size: 32,833 entries, 23 columns  
- Key Features: track name, artist, popularity, genre, danceability, energy, tempo, duration  

**Dataset 2: Most Streamed Spotify Songs (as of August 2024)**  
- Size: 953 entries, 25 columns  
- Key Features: track name, artist, streams, release year, popularity, danceability, energy  

Source Links:  
- [Spotify Songs Dataset](https://www.kaggle.com/datasets/joebeachcapital/30000-spotify-songs)  
- [Most Streamed Songs Dataset](https://www.kaggle.com/datasets/abdulszz/spotify-most-streamed-songs)  

## Analysis Summary

### Tempo and Genre

Using grouped analysis, we explored how tempo affects popularity across genres. The most popular combination was Latin songs between 176 and 200 BPM. However, statistical testing via ANOVA returned a p-value of 0.31, indicating no significant correlation.

### Energy Level

Scatter plots with regression lines across both datasets showed no strong correlation between energy level and streams. High energy extremes may have a slightly negative effect, but the impact is limited.

### Release Year

We found a weak negative correlation (r = -0.224) between release year and stream count, likely due to older songs having more time to accrue streams. More recent songs appear less popular on average due to time constraints.

### Danceability and Acoustics

Danceability showed a very weak positive correlation with popularity (r = 0.06), and acousticness had an even smaller correlation (r = 0.09). Neither variable showed strong predictive power alone.

## Machine Learning Model

A basic machine learning model was built to test whether popularity could be predicted using song features. The model achieved an accuracy of 77 percent on Dataset 1. While simple, this result suggests potential in using combined features for predictive modeling.

Notebook: `popularity_learning.ipynb`

## Conclusion

No single feature had a strong correlation with popularity, but a combination of many factors can be predictive. Machine learning offers a promising direction for future exploration of music analytics at scale.

## Reflections

While our hypotheses about individual features were largely unsupported, the project demonstrated how exploratory and statistical analysis can guide future questions and model development. Limitations included data clustering, sampling bias, and the evolving nature of Spotify's streaming algorithms.

## Repository Contents

- `datasets/` – Raw CSV data files
- `notebooks/` – Jupyter notebooks for each analysis question
- `popularity_learning.ipynb` – ML model for predicting song popularity
- `README.md` – Project overview
