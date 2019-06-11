# Data Modeling with Apache Cassandra

In this project data coming from audio streaming start-up had to be modeled in noSQL, denormalized manner and prepared for analytics. 

## Requirements

1. Python 3.x
2. Apache Cassandra 3.0+

## Data Structure

- **Denormalized tables**
    - **sessions_library** - the table letting to analyze data basing on particular sessions
        - session_id, item_in_session, artist, song_title, length
    - **user_library** - the table letting to analyze data basing on particular users
        - user_id, session_id, item_in_session, artist, song_title, first_name, last_name
    - **song_library** - the table letting to analyze data basing on particular songs
        - song_title, first_name, last_name

This time client was oriented on reads/writes considering big amounts of data. Horizontal scaling was also one of the most important requirements so Apache Cassandra seems to be an ideal choice for such a project.

## How to run a demonstrative ETL

Just open Jupyter Notebook `data_modeling_apache_cassandra.ipnyb` and run all cells. `CSV` file used to `INSERT` into database will be created during the work. 