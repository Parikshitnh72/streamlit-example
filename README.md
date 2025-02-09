YouTube Data Harvesting and Warehousing project

Problem Statement:

The problem statement is to create a Streamlit application that allows users to access and analyze data from multiple YouTube channels. The application should have the following features:
  Ability to input a YouTube channel ID and retrieve all the relevant data (Channel name, subscribers, total video count, playlist ID, video ID, likes, dislikes, comments of each video) using Google API.
 Option to store the data in a MongoDB database as a data lake.
 Ability to collect data for up to 10 different YouTube channels and store them in the data lake by clicking a button.
 Option to select a channel name and migrate its data from the data lake to a SQL database as tables.
Ability to search and retrieve data from the SQL database using different search options, including joining tables to get channel details.

Tools used:

Python
Google Client Library
MongoDB
MySQL
Streamlit 

Flow chart:

1. User Interface
   |
   v
2. Accept YouTube Channel ID and API Key
   |
   v
3. Use Google API to Retrieve Data
   |
   v
4. Display Retrieved Data in Streamlit
   |
   v
5. Data Storage Options
   |
   |---> [Store in MongoDB (Data Lake)]
   |     |
   |     v
   |     6. Store Channel, Video, and Comment Data
   |
   |---> [Store in SQL Database (Data Warehouse)]
         |
         v
         7. Data Modeling: Create Database Structure (MySQL)
         |
         v
         8. Transform and Store Data in MySQL
         |
         v
         9. Create Views for SQL Statements
         |
         v
         10. Display Data Analysis Results in Streamlit

Outcome:

Data harvesting: Using the "streamlit" Python library, which provides an interface for users to enter a YouTube channel ID and an API ID. Get data from YouTube videos and channels using the Python package for Google API client library.

Store semi-structured data in datalake: Store the fetched semi-structured data in a MongoDB database with 3 different collection names (Channels, Videos, Comments).

Data Modeling: Provided the SQL scripts with the foreign and primary key before starting the data transformation we have to create the database structure.

Transform data and store it in a data warehouse: Transfer data collected from multiple tables, i.e. channel, playlist, video and comment, to a SQL data warehouse, using a SQL database such as MySQL.

Data Analysis: The retrieved data is displayed within the Streamlit application and views are also created in the MySQL database for SQL statements that have more than one line.


