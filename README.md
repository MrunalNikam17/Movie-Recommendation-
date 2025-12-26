🎬 Movie Recommendation System (Content-Based)

A content-based movie recommendation system built using the TMDB 5000 Movies Dataset.
The system recommends movies similar to a given movie by analyzing genres, cast, crew (director), keywords, and overview text using NLP and cosine similarity.

🚀 Project Overview

This project recommends movies based on movie metadata similarity, not user ratings.
It uses Natural Language Processing (NLP) techniques to convert movie information into numerical vectors and then computes similarity scores.

Example recommendation for “Batman Begins”:

The Dark Knight
The Dark Knight Rises
Batman
Batman
Batman & Robin

🧠 How It Works (High-Level)

Load datasets (tmdb_5000_movies.csv, tmdb_5000_credits.csv)

Merge movies and credits data

Extract important features

Genres

Keywords

Top 3 Cast members

Director (from crew)

Movie overview

Create a unified text field (tags)

Text preprocessing

Lowercasing

Removing spaces in names

Stemming (Porter Stemmer)

Vectorization

Bag of Words using CountVectorizer

Similarity Calculation

Cosine Similarity

Recommendation

Return top 5 most similar movies

📂 Dataset Used

TMDB 5000 Movie Dataset

tmdb_5000_movies.csv

tmdb_5000_credits.csv

Each movie includes:

Title

Overview

Genres

Cast

Crew

Keywords

🛠️ Tech Stack & Libraries

Python

Pandas

NumPy

Scikit-learn

NLTK

🧪 NLP Techniques Used

Tokenization

Stopword removal

Stemming (Porter Stemmer)

Bag of Words (BoW)

Cosine Similarity

🧩 Feature Engineering

Each movie’s final tags field is created by combining:

overview + keywords + cast + genres + director


Example:

spacewar future alienplanet samworthington jamescameron action adventure

🔢 Vectorization
CountVectorizer(
    max_features=5000,
    stop_words='english'
)


Limits vocabulary size

Removes common English stopwords

Converts text into numerical vectors

📐 Similarity Metric

Cosine Similarity

Measures angle between two vectors

Values range from 0 (no similarity) to 1 (identical)
