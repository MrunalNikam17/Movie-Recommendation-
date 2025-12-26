# 🎬 Movie Recommendation System

**Content-Based Recommendation using NLP & Cosine Similarity**

<hr>

## 📌 Overview

This project implements a **content-based movie recommendation system** using the **TMDB 5000 Movies Dataset**.

The system recommends movies similar to a given movie by analyzing movie metadata and textual content such as:

- Movie overview  
- Genres  
- Keywords  
- Cast (top 3 actors)  
- Director  

It uses **Natural Language Processing (NLP)** and **Cosine Similarity** to find and rank similar movies.

<hr>

## 🎯 Example Recommendation

**Input Movie:** Batman Begins  

**Recommended Movies:**
The Dark Knight
The Dark Knight Rises
Batman
Batman
Batman & Robin

markdown
Copy code

<hr>

## 🧠 Recommendation Approach

This is a **content-based filtering system**, meaning:

- No user ratings are required  
- Recommendations are based purely on movie similarity  
- Ideal for cold-start problems  

<hr>

## ⚙️ How the System Works

### 1. Data Loading
- Load `tmdb_5000_movies.csv`
- Load `tmdb_5000_credits.csv`

<hr>

### 2. Data Merging
- Merge both datasets on the **title** column

<hr>

### 3. Feature Extraction

From raw JSON-like text fields:
- Genres  
- Keywords  
- Top 3 Cast Members  
- Director (from crew)  

<hr>

### 4. Feature Engineering

All relevant information is combined into a single column called **`tags`**:

overview + keywords + cast + genres + director

markdown
Copy code

<hr>

### 5. Text Preprocessing
- Lowercasing  
- Removing spaces between names  
- Tokenization  
- Stemming (Porter Stemmer)  

<hr>

### 6. Vectorization
- Bag of Words (BoW)
- CountVectorizer with:
  - `max_features = 5000`
  - English stopword removal  

<hr>

### 7. Similarity Calculation
- **Cosine Similarity** is used to compute similarity between movies

<hr>

### 8. Recommendation
- Top **5 most similar movies** are returned

<hr>

## 🛠️ Tech Stack

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- NLTK  

<hr>

## 📚 Dataset

**TMDB 5000 Movies Dataset**

- `tmdb_5000_movies.csv`
- `tmdb_5000_credits.csv`

Each movie contains rich metadata such as **genres, cast, crew, and plot summary**.

<hr>

## 🧪 NLP Techniques Used

- Tokenization  
- Stopword Removal  
- Stemming  
- Bag of Words (BoW)  
- Cosine Similarity  

<hr>
