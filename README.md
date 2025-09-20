# 🎬 Netflix Movies & TV Shows Analysis  

Analyze Netflix’s movie and TV show catalog using SQL to uncover insights like top-rated titles, most common genres, and actor/director statistics.  

## 📂 Dataset  
This project uses the **Netflix TV Shows and Movies** dataset (sourced from Kaggle).  
It contains metadata for thousands of Netflix titles, including:  
- `title`, `type` (Movie/Show), `release_year`, `genres`  
- `imdb_score`, `tmdb_score`, `tmdb_popularity`  
- `production_countries`, `age_certification`, `runtime`, `seasons`  
- `credits` (actors, actresses, directors, characters)  

## 📊 Features & Insights  
Key questions answered with SQL:  
- 🔝 **Top & Bottom Rated Titles**  
  - Top 10 movies and shows by IMDb score  
  - Bottom 10 movies and shows by IMDb score  
- 📈 **Score Statistics**  
  - Average IMDb & TMDB scores for movies and shows  
  - Average scores by production country and age certification  
- ⏳ **Trends Over Time**  
  - Count of movies and shows by decade  
  - Total titles released each year  
- 🎭 **Actors & Directors**  
  - Top 20 actors and directors by appearances  
  - Actors who starred in multiple highly rated titles  
  - Actors/actresses who played the same character in multiple titles  
- 🎥 **Genre Analysis**  
  - Most common genres for movies and shows  
  - Top 3 overall genres  
- ⌛ **Runtime & Seasons**  
  - Average runtime for movies vs. shows  
  - Shows with the most seasons on Netflix  

## 🛠️ Tools & Technologies  
- **SQL** – for data exploration and analysis  
- **SQLite/MySQL/PostgreSQL** – compatible database engines  
- **Kaggle Dataset** – [Netflix – TV Shows and Movies](https://www.kaggle.com/datasets/victorsoeiro/netflix-tv-shows-and-movies)  

## 🚀 Getting Started  

### 1️⃣ Clone the Repository  
```bash
git clone https://github.com/your-username/netflix-sql-analysis.git
cd netflix-sql-analysis

```

2️⃣ Load the Dataset

Place netflix_titles.csv into your database (e.g., import using SQLite or MySQL).

Use the provided SQL queries in queries.sql
 to recreate the analysis.

3️⃣ Run the Queries

Import the data and run:
-- Example: Top 10 Movies by IMDb Score
SELECT title, type, imdb_score
FROM shows_movies.titles
WHERE imdb_score >= 8.0 AND type = 'MOVIE'
ORDER BY imdb_score DESC
LIMIT 10;

## 📌 Example Insights

| 🎥 Top Movie             | ⭐ IMDb Score | 🌎 Country |
| ------------------------ | ------------ | ---------- |
| The Shawshank Redemption | 9.3          | USA        |
| The Godfather            | 9.2          | USA        |



