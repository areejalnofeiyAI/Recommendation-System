Spotify Recommendation System 🎵

A Hybrid Deep Learning Approach for Playlist Continuation
This repository contains a music recommendation system designed to solve the Automatic Playlist Continuation problem using deep learning techniques.
The project analyzes Spotify playlists from the Million Playlist Dataset (MPD) to understand user preferences and recommend tracks that fit the playlist’s overall mood and structure.

📌 Project Overview

Music playlists are more than just a list of songs — they reflect mood, taste, and listening behavior.
This project aims to capture these hidden patterns by combining:

Deep learning models (DAE & VAE)

Sentiment analysis on playlist titles

Unsupervised clustering techniques

The result is a recommendation engine that suggests songs that naturally follow the flow of a given playlist.

🧠 Methodology
1. Data Preprocessing

Playlist data is collected from multiple JSON files.

Features such as the number of tracks, artists, albums, playlist duration, and average song length are extracted.

Data is normalized for model training.

2. Sentiment Analysis

Playlist titles are analyzed using AFINN.

Each playlist is assigned a sentiment score (positive, negative, or neutral).

Sentiment is used as an additional feature to capture user intent.

3. Recommendation Models

🔹 Denoising Autoencoder (DAE)

Learns robust representations by reconstructing playlists from corrupted inputs.

Helps the model focus on essential playlist patterns.

Uses Mean Squared Error (MSE) as the loss function.


🔹 Variational Autoencoder (VAE)

Learns a probabilistic latent representation of playlists.

Uses KL Divergence to regularize the latent space.

Enables smoother and more meaningful recommendations.

4. Clustering (K-Means)

Applied to numerical playlist features.

Helps discover hidden patterns and group similar playlists.

Evaluated using the silhouette score.

📊 Exploratory Data Analysis (EDA)

Key insights from the dataset:

Average playlist length: ~66 tracks

Average song duration: ~3 minutes 54 seconds

Only ~2.1% of playlists are collaborative

Clear patterns in artist diversity, duration, and sentiment

🛠️ Tech Stack

Deep Learning: TensorFlow, Keras

Data Processing: Pandas, NumPy

NLP: AFINN

Machine Learning: Scikit-learn

Visualization: Matplotlib, Seaborn, Plotly
