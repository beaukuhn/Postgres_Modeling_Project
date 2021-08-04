# Project
Data Modeling with Postgres

#### Description
Sparkify has created a new music streaming app and wants to analyze which songs their users are listening to.
This code implements a schema for modeling their json data along with an ETL pipeline.

#### Design
A star schema design pattern was chosen, for Sparkify wants to analyze events -- songplays -- along with their affiliated models for granularity.

    Fact Table:
    songplays - records in log data associated with song plays i.e. records with page NextSong.
    
    Dimension Tables:
    users - users in the app; user_id, first_name, last_name, gender, level
    songs - songs in the music database; song_id, title, artist_id, year, duration 
    artists - artists in music database; artist_id, name, location, latitude, longitude
    time - timestamps of records in songplays broken down into specific units; start_time, hour, day, week, month, year, weekday
    
A simple ETL pipeline is used for data ingestion.

#### Contents

    data - directory containing pertinent project data 
    create_tables.py - script for creating SQL tables
    etl.ipynb - jupyter notebook for exploring ETL workflow
    etl.py - script implementing the ETL workflow
    requirements.txt - text file containing list of used packages
    sql_queries.py - script that defines project schema and affiliated query structure
    test.ipynb - jupyter notebook for exploring project testing

#### Installation
At the terminal, type `pip install -r requirements.txt`.

#### Run
To run the code, begin with entering `python create_tables.py` on the commandline, followed by `python etl.py`.

##### Jupyter Notebook
At the command line, enter `jupyter notebook`. Then, at a browser, type the URL http://localhost:8888. This will open the Jupyter Notebook interface, which allows easy access to notebook files.

##### Testing
Data must be first inserted into the database. For example, this can be done by running the Jupyter Notebook file `etl.ipynb`, followed by `test.ipynb`. 
