# Spotify Song Popularity Prediction

This project leverages machine learning to predict the popularity of songs on Spotify using various audio features. The project analyzes a dataset of over 32,000 songs and their characteristics to build predictive models.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Dataset](#dataset)
3. [Setup Instructions](#setup-instructions)
4. [Usage](#usage)
5. [Features](#features)
6. [Model Training and Evaluation](#model-training-and-evaluation)
7. [Contributing](#contributing)
8. [License](#license)

## Project Overview

The goal of this project is to predict the popularity of songs on Spotify based on their audio features. We use machine learning models to analyze various characteristics of songs and predict their popularity score (0-100).

## Dataset

The dataset contains 32,833 songs with 23 features including:
- Audio features (danceability, energy, key, loudness, mode, etc.)
- Track metadata (name, artist, album, release date)
- Playlist information (genre, subgenre)
- Popularity scores (target variable)

## Setup Instructions

1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   cd spotify_popularity_prediction
   ```

2. **Create a Virtual Environment**:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Run Jupyter Notebook**:
   ```bash
   jupyter notebook
   ```

## Usage

1. Open the `notebooks/spotify_popularity_prediction.ipynb` notebook in Jupyter
2. Follow the step-by-step analysis and model training process
3. The notebook is organized into sections:
   - Data Loading and Exploration
   - Data Preprocessing & Feature Engineering
   - Model Training
   - Model Evaluation

## Features

The project analyzes the following audio features:
- **Danceability**: How suitable a track is for dancing (0.0 to 1.0)
- **Energy**: Perceptual measure of intensity and activity (0.0 to 1.0)
- **Key**: The key the track is in
- **Loudness**: Overall loudness in decibels (dB)
- **Mode**: Modality (major or minor)
- **Speechiness**: Presence of spoken words (0.0 to 1.0)
- **Acousticness**: Confidence measure of acoustic quality (0.0 to 1.0)
- **Instrumentalness**: Predicts whether a track contains no vocals (0.0 to 1.0)
- **Liveness**: Detects presence of audience (0.0 to 1.0)
- **Valence**: Musical positiveness (0.0 to 1.0)
- **Tempo**: Estimated tempo in BPM
- **Duration**: Track length in milliseconds

## Model Training and Evaluation

The project uses three gradient boosting models:
- **XGBoost**
- **LightGBM**
- **CatBoost**

Each model is trained on the preprocessed dataset and evaluated using:
- Root Mean Square Error (RMSE)
- R-squared (R²)
- Mean Absolute Error (MAE)

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request for any improvements or bug fixes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
