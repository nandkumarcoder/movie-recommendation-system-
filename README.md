# Movie Recommendation System

A content-based movie recommendation system built using Python. This system recommends movies similar to a given movie based on features such as genres, keywords, cast, crew, and overview.

## Features

- **Content-Based Filtering**: Recommends movies based on their similarity to the input movie.
- **Data Preprocessing**: Cleans and processes movie data to extract meaningful features.
- **Cosine Similarity**: Measures the similarity between movies using vectorized tags.
- **Interactive Recommendations**: Allows users to input a movie title and get a list of similar movies.

## Dataset

- **TMDB 5000 Movies Dataset**: The dataset includes information about movies such as title, genres, keywords, cast, crew, and overview.
- Files used:
  - `tmdb_5000_movies.csv`
  - `tmdb_5000_credits.csv`

## Prerequisites

- Python 3.x installed on your system.
- Required Python libraries:
  - `numpy`
  - `pandas`
  - `nltk`
  - `scikit-learn`

## How It Works

1. **Data Loading**: The movie and credits datasets are merged on the `title` column.
2. **Feature Extraction**: Extracts relevant features such as genres, keywords, cast, crew, and overview.
3. **Data Cleaning**: Removes null values, duplicates, and unnecessary spaces.
4. **Tag Creation**: Combines all features into a single `tags` column for each movie.
5. **Vectorization**: Converts the `tags` column into numerical vectors using `CountVectorizer`.
6. **Similarity Calculation**: Computes cosine similarity between movie vectors.
7. **Recommendation**: Sorts and retrieves the top 5 most similar movies for a given input movie.

## How to Run

1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```
2. Navigate to the project directory:
   ```bash
   cd movie-recommendation-system-
   ```
3. Install the required libraries:
   ```bash
   pip install numpy pandas scikit-learn nltk
   ```
4. Place the dataset files (`tmdb_5000_movies.csv` and `tmdb_5000_credits.csv`) in the project directory.
5. Open and run the Jupyter Notebook (`movies recommendation.ipynb`) in your preferred environment.

## Example Usage

### Input:
```python
recomment('Avatar')
```

### Output:
```
Guardians of the Galaxy
Aliens
Star Trek Into Darkness
Star Trek Beyond
The Avengers
```

## File Structure

- `movies recommendation.ipynb`: The main notebook containing the implementation of the recommendation system.
- `tmdb_5000_movies.csv`: Dataset containing movie details.
- `tmdb_5000_credits.csv`: Dataset containing movie credits.

## Customization

- Modify the `tags` column creation logic to include additional features if needed.
- Adjust the `CountVectorizer` parameters (e.g., `max_features`) to fine-tune the recommendations.

## Libraries Used

- **Pandas**: For data manipulation and cleaning.
- **NumPy**: For numerical operations.
- **NLTK**: For stemming words in the `tags` column.
- **Scikit-learn**: For vectorization and similarity calculations.


## License

This project is licensed under the MIT License.

## Acknowledgments

- [TMDB Dataset](https://www.kaggle.com/tmdb/tmdb-movie-metadata) for providing the movie data.
- Inspired by content-based filtering techniques in recommendation systems.
