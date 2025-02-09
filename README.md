Million Song Dataset Analysis


Project Type: Music Data Analysis | Machine Learning | Recommendation System
Technologies Used: PySpark, Python, Machine Learning, Data Processing, Collaborative Filtering


Project Overview

This project explores how music metadata, user listening history, and audio features can be leveraged for data processing, classification models, and recommendation systems using the Million Song Dataset (MSD).


Key Objectives

- Music Data Processing: Understanding the structure, cleaning mismatches, and preparing datasets.
- Music Genre Classification: Training machine learning models to predict music genres based on audio features.
- Personalized Song Recommendation System: Implementing collaborative filtering (ALS) to recommend songs based on user listening behavior.


Project Structure

├── README.md                                            
├── Assignment2-Data Processing.ipynb       
├── Assignment2-Audio Similarity.ipynb      
├── Assignment2-Song Recommendations.ipynb  


Dataset Overview

This project is based on the Million Song Dataset (MSD), a large-scale dataset designed for music information retrieval (MIR) research. It was developed by The Echo Nest and LabROSA, later acquired by Spotify, making it a foundational dataset for music recommendation research.

Main Dataset Components
Song & Track Metadata: Includes song IDs, track IDs, artist names, release years, and 51 additional attributes.
Audio Features: Extracted using digital signal processing (DSP), including:
Loudness, tempo, beat, time signature
MFCC (Mel-frequency Cepstral Coefficients), spectral descriptors, rhythm patterns
User Listening History: Contains play counts for songs, reflecting user preferences.

Additional Datasets Used
Dataset Name	Description
Taste Profile	Contains user-song interaction data based on play counts. Used to build the recommendation system.
All Music Genre Dataset (MAGD)	Provides genre annotations derived from AllMusic, used for genre classification.

Data Challenges
Song-Track Mismatches:
~5,000 songs have incorrectly linked track IDs.
~13,000 track-song matches remain unverified.
Cold-Start Problem in Recommendations:
Many songs have limited listening history, making it difficult to recommend them effectively.


Project Workflow

Data Processing
- Explored dataset structure (file types, sizes, and data storage).
- Cleaned mismatched song-track pairs in the Taste Profile dataset.
- Mapped audio feature attributes to PySpark’s StructType.

Music Genre Classification
- Analyzed correlations between audio features to understand relationships.
- Merged genre labels with audio features for classification tasks.
- Trained classification models (Logistic Regression, Random Forest, GBTClassifier).
- Evaluated models using accuracy, precision, recall, and F1-score.

Personalized Song Recommendation System
- Filtered low-frequency songs and users to optimize model training.
- Trained ALS collaborative filtering model using user-song play history.
- Evaluated recommendations using Precision@10, NDCG@10, MAP@10.


Key Takeaways
- Used PySpark for scalable data processing on large datasets.
- Trained ML models to classify music genres from audio features.
- Built a collaborative filtering recommendation system with ALS.
- Analyzed and visualized large-scale user-music interactions.


References
- Million Song Dataset (MSD)
- AllMusic Genre Annotations
