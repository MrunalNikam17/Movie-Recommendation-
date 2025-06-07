🎬 Movie Recommendation System
This project recommends movies based on content similarity using Natural Language Processing (NLP) techniques. It is built using Python and focuses on analyzing movie metadata to suggest similar movies.

🚀 Features
Recommends movies based on title, genres, keywords, overview, cast, and crew.

Uses CountVectorizer and cosine_similarity to measure movie similarity.

Simple and intuitive function recommend('Movie Title') to get recommendations.

🧠 How It Works
Dataset Preprocessing:
Merges multiple metadata columns like genres, keywords, cast, and overview.
Cleans and processes text into a single tags field for each movie.

Vectorization:
Uses CountVectorizer to convert text data into numerical vectors.

Similarity Calculation:
Computes cosine similarity between movie vectors.

Recommendation:
For any given movie title, finds and returns the top 5 most similar movies.



🛠️ Libraries Used
pandas

scikit-learn

nltk (for optional preprocessing)

numpy
