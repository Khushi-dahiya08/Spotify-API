Project Overview
The Music Recommendation System recommends songs based on a user's input song list. It works by:

1. Using K-Means clustering to group songs in the dataset based on numerical features like energy, tempo, and danceability.
2. For a given list of input songs, it calculates their "average vibe" and recommends songs from the dataset with similar features.
3. The system integrates with the Spotify API to fetch additional song data (e.g., popularity, duration, and audio features).

Requirements
Python 3.x
Libraries:
numpy
pandas
sklearn
spotipy
scipy

To install the required libraries, you can use the following command:
pip install numpy pandas scikit-learn spotipy scipy

Usage:
1. Prepare Your Dataset: The dataset should be a CSV file that contains the information of songs, including features like energy, tempo,    acousticness, and others. Our sample dataset is provided along with this file
2. Spotify API Setup: You will need to create a Spotify Developer account and set up your Client ID and Client Secret. Visit Spotify Developer Dashboard to create your app and obtain these credentials.
3. Run the Script: You can now run the recommendation function in your Python environment. First, load your data, then call the recommend_songs() function with your input song list

Algorithm Explanation
This project uses K-Means clustering to group songs based on their features. The K-Means algorithm partitions songs into clusters, where each cluster contains songs with similar characteristics. When you provide a list of input songs, the system:

1.Calculates the average feature vector (mean vector) for the input songs.
2.Finds clusters in the dataset that are similar to the mean vector.
3.Recommends songs from those clusters.
Steps:
1.Pre-Clustering: The K-Means algorithm groups songs in the dataset into clusters based on their features (such as tempo, danceability, loudness, etc.).
2.Input Processing: When the user provides one or more songs, the system calculates the "average vibe" (mean vector) of these input songs.
3.Finding Similar Songs: The system compares the average vibe of the input songs to the songs in the dataset using cosine distance and recommends the closest matches.

Cosine Distance: Measures the similarity between vectors. Smaller distances indicate greater similarity between the input and the song in the dataset.

