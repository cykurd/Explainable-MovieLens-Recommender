# Explainable-MovieLens-Recommender
A hybrid movie recommender combining collaborative filtering (SVD) and content-based filtering to provide personalized suggestions with transparent explanations. Uses MovieLens data to explain recommendations by highlighting shared genres, themes, and similar user preferences.


This project is a hybrid recommendation system that combines collaborative filtering and content-based filtering, providing personalized movie recommendations along with intuitive explanations for each suggestion. Built with Python and utilizing the MovieLens Small dataset, this system offers an engaging, explainable approach to movie recommendations.

Features

	•	Collaborative Filtering (SVD): Uses Surprise’s SVD algorithm to capture user preferences based on ratings.
	•	Content-Based Filtering: Analyzes genres and tags to find content-similar movies.
	•	Hybrid Recommendations: Merges collaborative and content-based scores for balanced suggestions.
	•	Explanations for Recommendations: Explains each recommendation by detailing shared genres, themes, and similar user preferences.
	•	Adjustable Alpha Parameter: Allows tuning between collaborative and content-based contributions to hybrid score.

Dataset

The MovieLens Small dataset contains: 100,000 ratings and 3,600 tags for 9,000 movies rated by 600 users

This dataset provides both user interaction data (ratings) and metadata (genres, tags), ideal for a hybrid recommendation system.

Usage

	1.	Load Data: Import MovieLens data files (links, movies, ratings, tags) to load movie details and user ratings.
	2.	Training: Train the SVD model on the user ratings data to learn collaborative patterns.
	3.	Recommendation Generation: Use a favorite movie and user ID to generate recommendations.
	4.	Explanation Generation: Each recommendation includes reasons based on genres, themes, and similar user behavior.

Example Output

For a user whose favorite movie is “Toy Story (1995)”, the system might recommend:
	1.	Monsters, Inc. (2001)
Because it shares genres animation, fantasy, children, adventure, comedy, and users with similar preferences also liked it.
	2.	Toy Story 2 (1999)
Because it shares genres animation, fantasy, children, adventure, comedy, and has similar themes like pixar, and users with similar preferences also liked it.
	3.	The Emperor’s New Groove (2000)
Because it shares genres animation, fantasy, children, adventure, comedy, and users with similar preferences also liked it.

How It Works
1. Collaborative Filtering: Using SVD, the system learns user preferences by analyzing ratings patterns.
2. Content-Based Filtering: Each movie’s genre and tags are vectorized and compared to others using cosine similarity.
3. Hybrid Scoring: A weighted score merges collaborative and content-based scores, providing ranked recommendations.
4. Explainability: For each recommendation, genres and themes in common with the favorite movie are highlighted, along with insights from collaborative filtering.

