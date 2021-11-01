# Movies-ETL

## Project Overview

### Purpose

- Help Britta generate clean data sets for Amazing Prime hackathon organized to predict future popular movies low budget movies for better business profit.

- To develop an automated pipeline using python Pandas that takes in raw data in form of .csv and .json files, performs the appropriate transformations, and loads the data into existing SQL tables in PostgreSQL database. 

- Refactor the given code to create one function that takes in the three files—Wikipedia data, Kaggle metadata, and the MovieLens rating data, performs the ETL transformations and finally loads the clean transformed datasets to a PostgreSQL database.


### Background
Amazing Prime Video is a platform for streaming movies and TV shows on Amazing Prime the worlds largest online retailer. 
Their team wants to develop an algorithm to predict the low budget potentially popular movies that are being released so that they can buy the streaming rights for best possible deal. For this Amazing Prime has decided to sponsor a hackathon  for local coding community in order to have participants predict the popular pictures by providing a clean dataset.

## Resources
- Data Sourced from [IMDB](https://developer.imdb.com/?ref=ft_ds), [Kaggle](https://www.kaggle.com/):
  -  ratings.csv
  -  [movies_metadata.csv](https://github.com/Sheetaltkr/Movies-ETL/blob/main/Challenge/Resources/movies_metadata.zip) 
  -  [wikipedia-movies.json](https://github.com/Sheetaltkr/Movies-ETL/blob/main/Challenge/Resources/wikipedia-movies.json)
               
 - Software: Python 3.8.3, Jupyter Notebook, Anaconda 3, PostgreSQL 12, pgAdmin 4

## Stages of the ETL Pipeline

- **Extract**
  In this process we read the data in raw form and make it available for cleaning and transformation. For the Hackathon we are using wikipedia-movies.json,movies_metadata.csv     and ratings.csv. The source data format is different and needs to be converted into a common format for the next step.

- **Transform**
  Here the Data is transformed into a usable dataset that can be loaded into the database.  Data cleaning is performed which includes assessing the missing values, null values,   handling corrupt data, and formatting.  Then data is then  filtered, formatted, classified into understandable categories and finally merged. For our analysis we are merging     the movies data along with the Kaggle data by judiciously deciding on the best column values to keep among the 2 common columns from these datasets prior to merge. We then       merge the movies dataset with ratings dataset after converting the timestamp column values to standard format. 

- **Load**
  Once the data is transformed it is ready to be loaded into a database for analysis and reporting. We will be loading the dataset from python environment into PostgreSQL database in form of SQL tables.Post loading we check the count of movies table which 6,052 rows and the ratings table has 26,024,289 rows.

## Results
The result of this project is a [ETL function](https://github.com/Sheetaltkr/Movies-ETL/blob/main/Challenge/ETL_create_database.ipynb) that can be called to clean and transform any movie data from the given data sources and load it into SQL where further analyses can be performed.  

#### Movies table row count in PostgreSQL 
![movies table](https://github.com/Sheetaltkr/Movies-ETL/blob/main/Challenge/Resources/movies_query.png)

#### Ratings table load time during load process from Python environment to PostgreSQL 
![ratings table_load](https://github.com/Sheetaltkr/Movies-ETL/blob/main/Challenge/Resources/ratings_loadtime.png)

#### Ratings table row count in PostgreSQL 
![ratings table](https://github.com/Sheetaltkr/Movies-ETL/blob/main/Challenge/Resources/ratings_query.png)
