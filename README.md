# IMDb Data Cleaning & Feature Engineering Project

## 🔹 Project Overview
This project focuses on cleaning and enhancing the IMDb movies dataset.  
It demonstrates key **Data Cleaning** and **Feature Engineering** skills using Python and Pandas.  

The goal is to prepare a high-quality dataset ready for **data analysis** or **machine learning projects**.

---

## 🗂 Dataset
- Original dataset: `data/raw/imdb_raw.csv`
- Cleaned & enhanced dataset: `data/processed/imdb_clean.csv`
- Dataset contains popular movies with features like IMDb rating, genre, director, gross revenue, and more.

---

## 🧹 Data Cleaning Steps
1. Removed unnecessary columns:
   - Poster_Link, Overview, Certificate, Star2, Star3, Star4
2. Renamed columns for consistency (lowercase, snake_case)
3. Converted columns to proper data types:
   - released_year → numeric
   - runtime → numeric
   - gross → numeric
   - meta_score → numeric
4. Cleaned text columns:
   - genre → lowercase, stripped spaces
5. Handled missing values:
   - Dropped rows with missing critical values (imdb_rating, released_year, genre)
   - Filled numeric missing values with median (meta_score, gross)

---

## 🚀 Feature Engineering
New features were added to strengthen analysis and for CV impact:

| Feature | Description |
|---------|-------------|
| decade | Decade of movie release (e.g., 1990, 2000) |
| release_period | Categorized release period: Old / Middle / New |
| rating_category | IMDb rating category: Low / Average / High / Excellent |
| gross_category | Gross revenue category: Low / Medium / High |
| votes_per_million_gross | Popularity index combining votes and gross revenue |
| main_genre | First genre of the movie |
| genre_count | Number of genres for the movie |

---

## 🛠 Tools Used
- Python 3.x  
- Pandas library  
- Jupyter Notebook / VS Code  

---

## 📈 Final Dataset Columns
- series_title  
- released_year  
- runtime  
- genre  
- imdb_rating  
- meta_score  
- director  
- star1  
- no_of_votes  
- gross  
- decade  
- release_period  
- rating_category  
- gross_category  
- votes_per_million_gross  
- main_genre  
- genre_count  

---

## 🔗 How to Run
1. Clone the repository:  
```bash
git clone https://github.com/MahdiYaqobi/imdb-data-cleaning-project
```

2. Go to the project folder:  
```bash
cd imdb-data-cleaning-project
```

3. Install requirements:  
```bash
pip install -r requirements.txt
```

4. Run the notebook:  
```bash
python -m notebook
```

5. Open:  
`notebooks/imdb_data_cleaning.ipynb`


## 📊 Sample Insights
- Most movies are released after 2000
- High IMDb rating movies tend to have higher number of votes
- Multi-genre movies are more common in recent decades