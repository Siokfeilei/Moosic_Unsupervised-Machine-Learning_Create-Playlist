# Moosic_Unsupervised-Machine-Learning_Create-Playlist
Using unsupervised Machine Learning (scaling, principal components analysis PCA and KMeans clustering) to generate playlist from over 5000 Spotify songs based on audio features

## Overview
Moosic is a startup that creates curated music playlists based on specific moods and musical styles.  
As the platform grows, manually creating playlists becomes difficult to scale.

This project explores whether **unsupervised machine learning** can automatically generate playlists by clustering songs with similar audio characteristics.

## Objective
Use Spotify audio feature data to group songs into playlists using **K-Means clustering**.

## Dataset
The dataset contains approximately **5000 songs** with Spotify audio features including:

- Danceability
- Energy
- Tempo
- Valence
- Loudness
- Acousticness
- Instrumentalness
- Speechiness
- Liveness
- Duration
- Key and mode

These features describe musical properties such as rhythm, intensity, and emotional tone.

## Methodology

### 1. Data Exploration
Initial exploration helped understand how different audio features relate to perceived musical similarities.

### 2. Data Preprocessing
- Selected relevant features
- Scaled features using **MinMaxScaler**
- Prepared data for clustering using **NumPy arrays**

### 3. Clustering
- Applied **K-Means clustering**
- Determined optimal number of clusters using:
  - Elbow Method
  - Silhouette Score
- Ensured clusters produced playlists between **50–250 songs**

### 4. Dimensionality Reduction
Used **Principal Component Analysis (PCA)** to reduce noise and improve cluster separation.

## Results
The clustering algorithm generated multiple playlists grouping songs with similar musical characteristics.

While the clusters captured some meaningful musical similarities, certain aspects such as **lyrics, cultural context, and genre perception** were not represented in the dataset.

## Key Insights
- Spotify audio features can partially capture song similarity.
- Machine learning can assist in **scalable playlist generation**.
- Human curation may still be necessary to refine playlist quality.

## Technologies Used
- Python
- Pandas
- NumPy
- Scikit-Learn
- Matplotlib / Seaborn

## Future Improvements
- Incorporate **lyrics analysis**
- Include **genre metadata**
- Explore other clustering methods such as:
  - Hierarchical clustering
  - DBSCAN
- Build a recommendation system using **user listening behavior**
