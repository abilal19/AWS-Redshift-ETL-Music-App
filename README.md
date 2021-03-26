# AWS-Redshift-ETL-Music-App

## Introduction
 
There are two datasets being used in this project. The first is song metadata stored in data/song_data. This includes information about a song including who its artist is, how long the song is and information about the artist who created it including their name and location. These files are stored as JSON. An example is below:

{"num_songs": 1, "artist_id": "ARJIE2Y1187B994AB7", "artist_latitude": null, "artist_longitude": null, "artist_location": "", "artist_name": "Line Renaud", "song_id": "SOUPIRU12A6D4FA1E1", "title": "Der Kleine Dompfaff", "duration": 152.92036, "year": 0}

The other dataset is log data stored in data/log_data. These files are stored as JSON and include information about user activity for every session within the app. This includes information such as the userAgent used to access the app, the user's name, location, and what songs they have listened to. Each log file represents 1 day of user activity within the app.

## Setup
The files in this repo are as follows:

create_tables.py: python script to create the sparkify database or reset it

etl.py: python script to run the queries that extract the JSON data into staging tables in redshift and insert it into the dimensional tables which are also stored in redshift.

sql_queries.py: utilities file containing the PostgreSQL/Redshift queries that will be used to interact with the sparkify database.
dwh.cfg: configuration file that contains the settings required to connect to the redshift datawarehouse and run queries against it
