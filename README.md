### Data Modeling with Postgres: Sparkify ETL with Postgres
In this project we used Jupyter Notebook to learn about data modeling with Postgres and how to build an ETL pipeline using Python. 
To do this we followed the following steps:
1. Data modeling with Postgres
2. Creating star schema database
3. ETL pipeline using Python

## Project Description
We created a  SQL analytics database for Sparkify, a music streaming startup. Their analytics team wanted to understand what songs users are listening on their app.
Sparkify wanted an easy way to be able to query their data. The data are stored in raw JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.

# Project Data
The song dataset:  files are partitioned by the first three letters of each song's track ID
ex: {"artist_id": "ARD7TVE1187B99BFB1", "artist_latitude": null, "artist_location": "California - LA", "artist_longitude": null, "artist_name": "Casual", "duration": 218.93179, "num_songs": 1, "song_id": "SOMZWCG12A8C13C480", "title": "I Didn't Mean To", "year": 0}
The log dataset: files in the dataset are partitioned by year and month
ex: {"artist": "Stephen Lynch", "auth": "Logged In", "firstName": "Jayden", "gender": "M", "itemInSession": 0, "lastName": "Bell", "length": 182.85669, "level": "free", "location": "Dallas-Fort Worth-Arlington", "method": "TX PUT", "page": "NextSong", "registration": 1.540992.., "sessionId": "829", "song":"Jim Henson's Dead", "status": 200, "ts": 1543537327796, "userAgent": "Mozilla/5.0 (compatible; MSIE 10.0; Windows NT...", "userId": 91}

# Data modeling
For Sparkify we will use a relational database and use a Star Schema. A Star Schema is a multi-dimensional data model used to organize data in a database so that it is easy to understand and analyze, it can be applied to data warehouses, databases, data marts, and more. 
We will use this kind of database for a few reasons:
1. How the data we have is structured
2. The amount of data we have is not enough to need any Big Data databases
3. This structure will enable the analysts to aggregate the data in a easier manner
4. The ability to use SQL
5. We need to use JOINS for this scenario

## Project Template
This project will inlclude 6 files:
1. create_tables.py: drops and creates your tables. 
2. etl.ipynb: reads and processes a single file from song_data and log_data and loads the data into your tables.
3. etl.py: reads and processes files from song_data and log_data and loads them into your tables. (This is based on etl.ipynb)
4. sql_queries.py: contains all of the sql queries, it is imported into the last three files mentioned.
5. test.ipynb: displays the first few rows of each table, it is so you can check on your database.
6. README.md: provides a summary of the project, how to run the Python scripts, and an explanation of the files in the repository. It is this current file. 

