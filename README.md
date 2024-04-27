# Movies_Recommendation_system

Dataset Use : https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata?resource=download

# Movie Recommendation System with Content-Based Filtering
This system recommends movies based on their content (overview, genres, keywords) and how similar they are to a user's chosen movie. Here's the process breakdown:

1. Data Preparation:

Load movie data from a CSV file.
Clean text features (lowercase, remove punctuation, optionally stemming/lemmatization).
Combine overview, genres, and keywords into a single text feature.

2. Text Vectorization:

Choose either CountVectorizer or TF-IDF Vectorizer:
CountVectorizer: captures word frequency (how often a word appears)
TF-IDF Vectorizer: considers both word frequency and document frequency (how important a word is for a specific movie)
Create a document-term matrix where rows represent movies and columns represent unique words, with values indicating word importance based on the chosen vectorizer.

3. Recommendation Engine:

Define a function to generate recommendations:
Find the chosen movie's index in the data.
Calculate cosine similarity between the chosen movie and all other movies using the document-term matrix. This measures how similar their content is.
Sort movies by cosine similarity (most similar first).
Return the top k most similar movies (excluding the chosen movie)

![recommendation](https://github.com/tariqahmedproject/Movies_Recommendation_system/blob/main/Movie%20Recomend.JPG)
