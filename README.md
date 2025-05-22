# Movies-Recommendation-System
This project develops a movie recommendation system using collaborative filtering, predicting user preferences based on past ratings. It identifies similarities between users or movies to generate personalized suggestions. Built with Pandas, NumPy, and Scikit-learn, it employs cosine similarity to detect patterns in user interactions.

Dataset
 The dataset used here is from https://github.com
 The system uses the MovieLens dataset:
 • u.data: Contains user ratings for movies (user ID, movie ID, rating, times
tamp).
 • u.item: Provides movie information (movie ID, title). These datasets are
 merged to create a structured user-movie rating matrix.
 Methodology
 
 We apply collaborative filtering, which can be broken into two types:
 • Item-based filtering (Finding similar movies based on user ratings).
 • User-based filtering (Recommending movies by analyzing preferences of
 similar users).
 
 # To compute similarity, we use cosine similarity:
 • Movie similarity matrix: Helps recommend movies similar to a given title.
 • User similarity matrix: Suggests movies by identifying users with similar
 tastes.

 
 Evaluation Metrics:
 We evaluate the recommendation system using:
 • RMSE (Root Mean Squared Error): Measures prediction accuracy by
 comparing actual and predicted ratings.
 • Precision@k: Assesses recommendation relevance by counting how many
 top-K recommended movies align with the user’s high-rated selections.

Usage Instructions
 To Get Similar Movie Recommendations:
 print(get_movie_recommendations(“Toy Story (1995)”, 5)) This suggests 5
 movies similar to “Toy Story (1995)”.
 
 To Get User-Based Movie Recommendations:
 print(recommend_movies_for_user(300)) This provides recommendations for
 user 300 based on similar users’ preferences.

 To Evaluate Performance:
 print(“RMSE:”, rmse) print(“Precision@5:”, precision_at_k(recommended_movies,
 relevant_movies, 5)) This will print the accuracy metrics for validation.
 
 Final Thoughts
 This recommendation engine demonstrates the power of collaborative filtering in
 predicting user preferences. While it performs well, improvements like matrix
 factorization or deep learning techniques could further enhance accuracy.
