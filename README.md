# FilmFinder: A Multi-Algorithm Movie Recommendation Engine

## Overview
This project implements a movie recommendation system using the MovieLens 20M dataset. It employs various recommendation algorithms, including popularity filtering, content-based filtering, collaborative filtering, and integrates natural language processing (NLP) with Hugging Face's models. The goal is to provide personalized movie recommendations based on user preferences and behaviors.

## Table of Contents
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Evaluation](#evaluation)
- [License](#license)

## Features
- **Popularity-Based Recommendations**: Suggests movies based on their popularity among users.
- **Content-Based Filtering**: Recommends movies based on genres and descriptions using TF-IDF and cosine similarity.
- **Collaborative Filtering**: Uses the SVD algorithm to predict user preferences based on past ratings.
- **LLM Integration**: Implements NLP capabilities using Hugging Face's transformers to enhance recommendations.
- **Performance Evaluation**: Measures the effectiveness of recommendations using precision and recall metrics.

## Technologies Used
- Python
- Pandas
- NumPy
- scikit-learn
- Surprise (for collaborative filtering)
- Hugging Face Transformers

- Jupyter Notebook (or any Python environment)

## Dataset
The dataset used for this project is the **MovieLens 20M dataset**. It contains 20 million ratings from users, along with movie titles and genres.

- [MovieLens 20M Dataset - Download]([https://grouplens.org/datasets/movielens/20m/](https://www.kaggle.com/datasets/grouplens/movielens-20m-dataset))

To use the dataset, you will need to download the following CSV files:
- `movies.csv`: Contains movie IDs, titles, and genres.
- `ratings.csv`: Contains user IDs, movie IDs, ratings, and timestamps.

## Installation
1. Clone the repository:

   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. Install the required packages:

   ```bash
   pip install pandas numpy scikit-learn surprise transformers
   ```

## Usage
1. Load the dataset by ensuring the `movies.csv` and `ratings.csv` files are in the correct directory.
2. Run the script or Jupyter Notebook to execute the recommendation algorithms.
3. Modify the `true_positive_movies` list in the code to include movies that you want to evaluate the recommendations against.
4. View the results printed in the console, which include precision and recall for each recommendation method along with the recommended movies.

### Example Code Snippet
```python
# Generate Recommendations
user_id = 1
pop_recs = popularity_recommendations()
content_recs = content_based_recommendations('Toy Story (1995)')
collab_recs = collaborative_recommendations(user_id)

# Evaluate Recommendations
evaluate_recommendations(true_positive_movies, pop_recommendations)
```

## Evaluation
The recommendation system's performance is evaluated using precision and recall metrics. The results are displayed for each recommendation method, indicating how effectively the system can recommend relevant movies based on the user's preferences.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Feel free to update the sections based on your project's specific requirements, add any additional instructions, or modify any content that better suits your project style. Let me know if you need any further modifications!
