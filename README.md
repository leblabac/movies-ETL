# Movies-ETL
This project was an introduction ot the EXTRACT, TRANSFORM, and LOAD process. Movie data from Wikipedia, Kaggle, and aggregated ratings were used to assemble a movie database for a fictional hackathon.

## Overview
The goal of this analysis is to create an automated pipeline that extracts, transform and loads data. Each step built on the other, and the final clean data output was added to a PostGres database. The overall process was broken down into four jupyter notebook files:

### ETL_function_test.ipynb
- Data was extracted from the websites in their native formats and then transformed into Pandas DataFrames

### ETL_clean_wiki_movies.ipynb
- The movie list was cleaned and columns merged where applicable
- Only columns that did not have null values were kept
- Data was parsed using Reg expressions to align in for the final table
- Box office, budget, release date and run time were all cleaned from the wiki movies table

### ETL_clean_kaggle_data.ipynb
- Function extract_transform_load gets new tasks for cleaning Kaggle data

### ETL_create_database.ipynb
- The final step connects the cleaned data to the database by sqlalchemy library and to_sql method.

## Summary 
In summary, the complete ETL process can (by the fourth document) be executed with a single function extract_transform_load call.
