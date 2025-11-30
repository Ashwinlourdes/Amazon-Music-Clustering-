# 🎵 Amazon Music Clustering Dashboard
Unsupervised Machine Learning Project for Song Grouping & Audio Feature Analysis

This project analyzes Amazon Music songs and groups them into meaningful clusters using K-Means Clustering.
It includes an interactive Streamlit Dashboard to explore clusters, visualize patterns, and understand the musical characteristics of each group.

🚀 Features & Highlights

🎧 Automatic grouping of songs using K-Means

📊 Interactive visualizations (PCA plots, heatmaps, bar charts)

🧠 Cluster profiling – understand average characteristics of each group

📋 Audio feature analysis (energy, valence, acousticness, etc.)

📈 Evaluation metrics (Silhouette Score, Davies-Bouldin Index)

📥 Export clustered dataset as CSV

🖥️ User-friendly dashboard built using Streamlit

📂 Project Structure
📁 project-folder
│── amazon.py                 # Main Streamlit dashboard
│── cleaned_data.pkl          # Preprocessed dataset + KMeans + PCA + metrics
│── clean.ipynb               # Data cleaning & preprocessing notebook
│── README.md                 # Project documentation

🧠 Project Workflow (Step-by-Step)
1️⃣ Data Preprocessing

Performed in clean.ipynb:

Load raw dataset

Clean missing / inconsistent data

Select numeric audio features

Apply Standard Scaling

Apply PCA transformation for 2D visualization

Run K-Means to generate cluster labels

Create cluster profiles (mean values per cluster)

Save all objects inside cleaned_data.pkl

2️⃣ Streamlit Dashboard

The app (amazon.py) loads:

df_reference (original data + clusters)

scaled data

PCA results

cluster labels

cluster summary statistics

evaluation metrics

3️⃣ Model Used: K-Means Clustering

Unsupervised ML algorithm

Groups similar songs based on audio features

Ideal for numeric feature comparison

Evaluated using:

Silhouette Score

Davies-Bouldin Index

🖥️ Running the Dashboard Locally
1. Install dependencies
pip install streamlit pandas matplotlib seaborn scikit-learn

2. Run Streamlit App
streamlit run amazon.py

3. Make sure the pickle file is present

Place your cleaned_data.pkl in the same folder as amazon.py.

🎨 Dashboard Pages
🔹 Overview

Project intro

Dataset summary

Cluster distribution

Top 5 songs

🔹 Metrics

Silhouette Score

Davies-Bouldin Index

Cluster summary table

🔹 Visualizations

PCA 2D scatter plot

Heatmap of cluster means

Key feature comparison bar chart

🔹 Insights & Export

Top songs per cluster

Easy-to-understand cluster interpretations

Download full clustered dataset (CSV)

📊 Example Cluster Interpretations

Cluster 0: High energy → Party songs

Cluster 1: Low energy, acoustic → Chill / relaxing tracks

Cluster 2: Balanced mood → General listening

Cluster 3: Instrumental-heavy → Focus / study tracks

These are based on cluster mean values inside the profile.

📈 Evaluation Metrics
Metric	Description
Silhouette Score	Measures cluster separation (higher = better)
Davies-Bouldin Index	Measures cluster similarity (lower = better)

Both metrics are loaded and displayed in the dashboard.

🛠️ Tech Stack Used

Python

Streamlit

Pandas & NumPy

Scikit-learn (KMeans, StandardScaler, PCA)

Matplotlib & Seaborn (visualizations)

Pickle (model/data storage)

🧩 Applications

Music recommendation systems

Mood-based playlist generation

Artist similarity discovery

Music analytics dashboards

Organizing large music catalogs

⚠️ Limitations

Fixed number of clusters (K chosen beforehand)

PCA reduces feature information

Only audio features used (no tempo, loudness, key, etc.)

No retraining or custom clustering inside UI

🚀 Future Improvements

Allow user to choose number of clusters dynamically

Add more music features (tempo, key, loudness)

Add genre-level insights

Build a song recommendation engine

Deploy the app online using Streamlit Cloud or HuggingFace Spaces

🙌 Acknowledgements

Amazon Music dataset (or source used)

Streamlit for app framework

Scikit-Learn for clustering algorithms

Matplotlib / Seaborn for plots
