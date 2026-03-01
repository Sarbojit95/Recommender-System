Hybrid Recommender System – IBM Articles

Overview



This project builds a multi-strategy recommender system for IBM article data using user interaction history and article titles. The goal is to recommend relevant articles under different user scenarios (cold start, sparse history, rich history).



The system implements and compares four recommendation approaches.



Methods Implemented

1\. Rank-Based Recommendations



Recommends most popular articles based on interaction counts.



Handles cold-start users with no history.



2\. User-User Collaborative Filtering



Uses cosine similarity on a user-item matrix.



Recommends articles from similar users.



Improved with deterministic ranking (similarity + interaction count).



3\. Content-Based Filtering



TF-IDF vectorization on article titles.



Dimensionality reduction via Truncated SVD (LSA).



KMeans clustering for semantic grouping.



Recommends similar articles ranked by popularity.



4\. Matrix Factorization (SVD)



Performs SVD on user-item interaction matrix.



Uses latent features to compute cosine similarity between articles.



Captures deeper interaction-driven structure.



Cold-Start Strategy



New users : Rank-based + Content-based.



Light-history users : Content-based + Collaborative filtering.



Heavy users : SVD-based personalized recommendations.



A hybrid approach balances robustness and personalization.



Evaluation Approach



To determine improvement over baseline methods:



Offline metrics: Precision, Recall.



Online metrics: Click-through rate, dwell time.



A/B testing for real-world validation.



Tech Stack



Python



Pandas, NumPy



Scikit-learn (TF-IDF, KMeans, SVD, Cosine Similarity)



Matrix factorization



Key Learnings



Building recommendation systems requires careful ranking logic and tie-breaking.



Different methods perform better at different stages of user maturity.



Hybrid systems are typically more stable and scalable than single-method approaches.

