# Movies-ETL

## Project Overview

### Purpose

- Help Britta generate clean data sets for Amazing Prime hackathon organized to predict future popular movies low budget movies for better profit.

- To develop an automated pipeline that takes in raw data, performs the appropriate transformations, and loads the data into existing tables. 

- Refactor the given code to create one function that takes in the three files—Wikipedia data, Kaggle metadata, and the MovieLens rating data, performs the ETL transformations and finally loads the clean transformed datasets to a PostgreSQL database.


### Background
Amazing Prime Video is a platform for streaming movies and TV shows on Amazing Prime the worlds largest online retailer. 
Their team wants to develop an algorithm to predict the low budget potentially popular movies that are being released so that they can buy the streaming rights for best possible deal. For this Amazing Prime has decided to sponsor a hackathon  for local coding community in order to have participants predict the popular pictures by providing a clean dataset.

## Resources
- Data Sourced from [IMDB](https://developer.imdb.com/?ref=ft_ds), [Kaggle](https://www.kaggle.com/):
  -  ratings.csv
  -  [movies_metadata.csv](https://github.com/Sheetaltkr/Movies-ETL/Challenge/Resources/movies_metadata.csv) 
  -  [wikipedia-movies.json](https://github.com/Sheetaltkr/Movies-ETL/Challenge/Resources/wikipedia-movies.json)
               
 - Software: Python 3.8.3, Jupyter Notebook, Anaconda 3, PostgreSQL 12, pgAdmin 4

## Stages of the Pipeline

- **Extract**- Data is read into the python environment using Pandas from two differing formats; csv and json.  

- **Transform**- Data is transformed into a usable dataset that can be loaded into the database.  Data cleaning included assessing missing values, null values, handling corrupt data, and formatting.  Then data was filtered, formatted, classified into understandable categories, and finally merged.

- **Load**- Created a connection to the database from the python environment and loaded in the final dataset.

## Results
The result of this project is a [single function](https://github.com/Sheetaltkr/Movies-ETL/Challenge/ETL_create_database.ipynb) that can be called to clean and transform any movie data from the given data sources and load it into SQL where further analyses can be performed.  
