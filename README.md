# Musik Empfehlung : RhythMatch
Music-Recommendation


Key Features:
      1.	Recommendation Engine:
                    Combines audio-based features (e.g., danceability, energy) and metadata features (genre, tags) to identify songs similar to user-selected tracks. Incorporates cosine                              similarity and customizable weighting to adapt to user preferences.
      2.	Interactive Dashboard:
            A user-friendly interface built using Streamlit, allowing users to:
            o	Explore personalized recommendations.
            o	Filter by artist and adjust similarity preferences (audio vs. metadata).
            o	Gain insights into user trends and song popularity.
      3.	Transparency:
      Provides clear reasoning behind recommendations, emphasizing audio-based matches or metadata alignment (genre/tags).

Objectives :
      1.	Personalized Music Suggestions: Recommend songs based on user behavior and listening history.
      2.	Enhanced User Engagement: Keep users engaged with dynamic and relevant song recommendations.
      3.	Music Discovery: Help users explore new genres and artists beyond their typical choices.


Methodology :
      
      1.	Dataset Preparation:
          o	Missing values in genre and tags columns are filled with empty strings to avoid errors during processing.
          o	Combined text features (genre + tags) are created for text-based similarity calculations.
          
      2.	Feature Extraction:
          o	Numeric Features: Extracted directly from the dataset (e.g., danceability, energy). These features represent the audio-based characteristics of a song.
          o	Text Features: TF-IDF is applied to the combined text column to create vector representations of genre and tags.
          
      3.	Similarity Calculations:
          o	Numeric Similarity: Calculated using cosine similarity on numeric features.
          o	Text Similarity: Calculated using cosine similarity on TF-IDF vectors.
          o	Weighted Combination: Both similarities are combined into a single score based on user-defined weights.
          
      4.	Recommendation Logic:
          o	Top 5 most similar songs are selected based on the combined similarity score.
          o	Reasoning for each recommendation is dynamically generated using audio features or metadata, depending on the dominant similarity.
          
      5.	UI and User Interaction:
          o	Users can filter songs by artist, adjust similarity preferences (audio vs. genre/tags), and select a song to receive tailored recommendations.
          o	Audio previews are displayed if available.
