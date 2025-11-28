# 🎵 **Checkpoint 1 – Baseline Music Recommender**

This checkpoint focuses on preparing the dataset and building a simple baseline recommendation system for the **Interactive Mood-Based Music Recommender** project.

---

## ✅ **1. Overview**

In this checkpoint, we prepared the Spotify dataset, explored its features, and built a **baseline model** using cosine similarity.
This model recommends similar songs based on their audio characteristics.



## ✅ **2. Work Completed**

### **✔ Data Loading**

* Loaded the Spotify dataset from Kaggle
* Reduced the dataset to **10,000 tracks** to avoid memory issues
* Previewed the data using `df.head()` and `df.shape`

### **✔ Data Cleaning**

* Selected only **numeric audio features** (energy, valence, tempo, danceability, etc.)
* Removed unnecessary columns
* Ensured the data was ready for numerical operations

### **✔ Exploratory Data Analysis (EDA)**

* Created histograms for:

  * **Energy**
  * **Valence**
* Generated a **correlation heatmap** to inspect relationships between audio features

### **✔ Data Scaling**

* Applied `StandardScaler` to normalize audio features
* Scaling ensures all features have equal importance when computing similarity

### **✔ Baseline Recommendation Model**

* Computed a **cosine similarity matrix** for 10,000 songs
* Implemented a `recommend()` function that:

  * Takes a song name as input
  * Returns a list of similar tracks
* Successfully tested the baseline recommender



## ✅ **3. Challenges & Solutions**

### **⚠️ Large Dataset → Memory Error**

The original dataset (232k songs) caused memory issues when computing similarity.
**Solution:**
Reduced the dataset to 10,000 rows.

### **⚠️ String Columns Causing Errors**

Some columns were non-numeric (track name, artist, genre).
**Solution:**
Selected only numeric columns for scaling and similarity.


