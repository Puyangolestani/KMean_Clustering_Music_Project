# KMean_Clustering_Music_Project

# 🎧 Turning Data Into Vibes: Building Spotify Playlists with KMeans Clustering

This repository presents a data science project that leverages KMeans clustering to create curated Spotify playlists based on song audio features and lyrics.

🔗 **[Explore the Code on Google Colab](https://colab.research.google.com/drive/1gQiQpyL7YaasYzkBvBihA_NR4WqNEbNw?usp=sharing)**

---

## 📊 Project Overview

This project demonstrates how Spotify’s audio features and song lyrics can be used to algorithmically group similar songs into playlists. The workflow includes:

- **Data Scaling:** Using `MinMaxScaler` to normalize audio features, ensuring no single feature dominates due to scale differences.
- **Lyrics Vectorization:** To incorporate lyrical content, `TfidfVectorizer` is used to convert lyrics into numerical arrays. This method transforms text into a matrix of TF-IDF (Term Frequency–Inverse Document Frequency) scores, capturing the relative importance of words in each song. These vectors are then combined with audio features to enrich the clustering process.
- **Cluster Estimation:** Determining the optimal number of clusters (`k`) using:
  - **Inertia/Elbow Method:** Identifies the "elbow point" where adding more clusters yields diminishing returns in compactness.
  - **Silhouette Score:** Measures how similar each song is to its own cluster compared to others — higher scores indicate better-defined clusters.
- **Playlist Generation:** Applying the KMeans algorithm with the selected `k` to group songs into clusters (playlists) based on their audio and lyrical characteristics.

---

## 💼 Business Implications

The approach has several practical and commercial advantages:

- **Enhanced Authenticity:** Curate playlists that feel more intentional, with distinct moods, genres, or lyrical themes.
- **Effective A/B Testing:** Test playlist variations and measure listener engagement more accurately.
- **Smarter Recommendations:** Improve song placement and listener targeting through more granular clustering.
- **Scalable Playlist Management:** Easily adjust, split, or merge playlists as your catalog grows.

---

## 🎵 Playlist Examples

An example playlist, **"After Work Vibes"**, included a mix of Gospel, Bossa Nova, and Jazz — suggesting that initial clustering may group songs by audio feel rather than strict genre. This opens the door for further refinements, such as:

- Genre-specific playlists (e.g., Brazilian Jazz only)
- Mood-focused lists (e.g., relaxing vs. energetic)
- Filtering songs (e.g., removing Gospel if not suitable for all listeners)

---

## ⚠️ Limitations

While KMeans provides a helpful foundation, there are several limitations:

- **Hard Clustering Only:** Each song belongs to a single cluster, even if it fits multiple moods or genres.
- **Manual `k` Selection:** Clustering effectiveness depends on choosing the right number of clusters.
- **Subjectivity of Music:** Neither audio features nor lyrics can fully capture the human emotional or cultural response to music.

---

## 🚀 Future Development

Potential enhancements to this project include:

- Exploring other clustering algorithms (e.g., DBSCAN, GMM, hierarchical)
- Combining audio/lyrics with collaborative filtering or content-based recommendation engines
- Integrating user feedback to fine-tune playlist clusters over time

---

## 📎 Access the Code

You can explore and run the full notebook in Google Colab here:  
👉 **[Google Colab Notebook](https://colab.research.google.com/drive/1gQiQpyL7YaasYzkBvBihA_NR4WqNEbNw?usp=sharing)**
