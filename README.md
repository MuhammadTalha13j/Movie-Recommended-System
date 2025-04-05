# 🎬 Movie Recommender System

A content-based movie recommendation system that suggests similar movies based on genres, keywords, cast, crew, and overview. Built with Streamlit for the UI and powered by TMDb data.

## Features
- Recommends 5 movies similar to the user's selection.
- Displays movie posters fetched from TMDb API.
- Responsive and interactive UI powered by Streamlit.

## Data Sources
- [TMDb 5000 Movies Dataset](https://www.kaggle.com/tmdb/tmdb-movie-metadata)
- [TMDb 5000 Credits Dataset](https://www.kaggle.com/tmdb/tmdb-movie-metadata)

## How It Works
1. **Data Preprocessing**:
   - Merges movie metadata and credits data.
   - Extracts genres, keywords, top 3 cast members, and directors.
   - Combines features into a "tags" column for text processing.
   - Applies stemming and vectorization using `CountVectorizer`.

2. **Similarity Calculation**:
   - Uses cosine similarity to find movies with comparable tags.

3. **Recommendation Engine**:
   - Fetches posters via TMDb API.
   - Returns top 5 matches based on similarity scores.

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/movie-recommender.git
   cd movie-recommender

movie-recommender/
├── app.py               # Streamlit application
├── MRS.ipynb            # Data preprocessing and model training
├── movie_dict.pkl       # Preprocessed movie data
├── similarity.pkl       # Precomputed similarity matrix
└── README.md

  
  pip install streamlit pandas numpy scikit-learn nltk requests
