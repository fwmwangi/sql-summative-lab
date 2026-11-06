# IMDB Movie Dataset: Exploratory Data Analysis (2010-2019)

## Project Overview
This project involves an exploratory data analysis (EDA) of an IMDB movie dataset using SQL and Python. The primary objective is to query a relational database to uncover trends in movie production, audience ratings, and runtimes for films released between 2010 and 2019. The insights generated from this analysis are designed to answer specific business questions regarding the commercial viability of different movie genres.

## Problems Solved & Methodology
During this lab, several data cleaning and exploratory tasks were performed to ensure accurate analysis:
*   **Data Filtering:** Enforced strict date boundaries by filtering the database for movies released specifically between 2010 and 2019.
*   **Handling Missing Data:** Cleaned the dataset by identifying and excluding null values in critical fields, particularly `runtime_minutes`, `genres`, and `averagerating`.
*   **Complex SQL Joins:** Connected multiple tables (`movie_basics` and `movie_ratings`) to bridge descriptive movie data with audience reception metrics.
*   **Categorization:** Used SQL `CASE` statements to group continuous variables (like runtime) into categorical bins (e.g., 'Under 60 min', '90-120 min') for easier trend identification.

## Key Findings
1.  **Runtime Trends:** The analysis revealed a correlation between specific runtime categories and higher audience reception, pointing toward an optimal "sweet spot" for movie length.
2.  **Genre Performance vs. Volume:** By analyzing the average ratings of genres against the total number of movies produced in those genres, we identified which categories yield the highest average ratings while maintaining a production volume that demonstrates commercial viability (filtering out highly-rated but overly niche genres).

## Business Question Addressed
*"Based on the performance data from 2010-2019, which specific genres yield the highest average ratings while maintaining a production volume that demonstrates commercial viability, and what is the optimal target runtime for these high-performing genres?"*

## Repository Contents
*   `SQLSummativeLab.ipynb`: The main Jupyter Notebook containing the Python code, SQL queries (via `sqlite3` and `pandas`), and data visualizations.
*   `data.sqlite`: A subset of the database used for initial testing and querying.
*   `Images/`: Directory containing generated data visualizations (e.g., Seaborn/Matplotlib bar charts).
*   `gitignore.txt`: Standard gitignore file for Python/Jupyter projects.
*   *(Note: The full `im.db` database file is excluded from this repository due to GitHub size constraints, but the notebook contains all the reproducible queries used to extract the data).*

## Tools & Technologies Used
*   **Languages:** SQL, Python 3
*   **Libraries:** Pandas, Matplotlib, Seaborn, sqlite3
*   **Environment:** Jupyter Notebook