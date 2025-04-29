# Spotify Song Popularity Prediction

This project builds a machine learning pipeline to predict Spotify song popularity based on audio features.  
It explores the extent to which a song’s success can be predicted using characteristics like energy, danceability, and tempo.

# <img src="./Images/logo.png" alt="Logo" width="400">

## Project Overview

The goal is to predict the **popularity score (0–100)** of Spotify songs using audio-based features.  
Gradient boosting models — **XGBoost**, **LightGBM**, and **CatBoost** — were trained, tuned, and compared.

The project demonstrates the challenges of predicting complex human preferences with structured data.

## Dataset

The dataset contains metadata and audio attributes for **32,833 songs**.  
For full details, see the [README in the `data/` folder](./data/README.md).

Key features include:
- Audio characteristics (danceability, energy, loudness, speechiness, valence, etc.)
- Release metadata (release year, track age)

## Feature Engineering

- Cyclical encoding of musical key
- Derived features (e.g., energy-to-danceability ratio, acoustic-energy balance)
- Release time features (track age, release month/day/year)
- Mood-based features combining valence and energy

## Model Training and Evaluation

Three gradient boosting models were trained with hyperparameter tuning and 3-fold cross-validation:

| Model     | RMSE   | R² Score | MAE   |
|:----------|:------:|:--------:|:-----:|
| XGBoost   | 21.10  | 0.283    | 17.35 |
| LightGBM  | 20.50  | 0.323    | 16.74 |
| CatBoost  | 21.42  | 0.261    | 17.77 |

- **LightGBM** achieved the best performance across all metrics.
- **XGBoost** was close, while **CatBoost** slightly underperformed in this setup.

Evaluation was based on:
- Root Mean Squared Error (RMSE)
- R-squared Score (R²)
- Mean Absolute Error (MAE)
- Residual Analysis

## Results and Conclusion

- **Predictive power was modest** — models explained only ~30% of the variance in song popularity.
- Audio features alone are **insufficient to fully predict popularity**, which is influenced by many external factors like marketing, artist fame, and social trends.
- **Feature engineering improved results**, but residual variance remained high.

> Despite the inherent challenges, this project successfully demonstrates the structured application of machine learning to real-world music data, highlighting the limitations and potential of predictive modeling in the entertainment industry.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
