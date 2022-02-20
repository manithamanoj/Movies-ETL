# Movies-ETL
# Introduction

In this challenge we are going to create an automated pipeline that takes in new data, performs the appropriate transformations, and loads the data into existing tables. We need to refactor the code from this module to create one function that takes in the three files -Wikipedia data, Kaggle metadata, and the MovieLens rating data, and performs the ETL process by adding the data to a PostgreSQL database.

## Analysis

Write an ETL Function to Read Three Data Fileswith the help of Python, Pandas, the ETL process, and code refactoring, and creates three separate DataFrames.

•	The wiki_movies_df DataFrame

<img width="1299" alt="Screen Shot 2022-02-19 at 11 16 52 PM" src="https://user-images.githubusercontent.com/72629108/154831130-8259b595-255b-44d7-8ced-9ab2f53d67a3.png">

•	The kaggle_metadata DataFrame
<img width="1295" alt="Screen Shot 2022-02-19 at 11 17 14 PM" src="https://user-images.githubusercontent.com/72629108/154831156-ef53be63-79c3-4ead-ae14-e8f14aed0101.png">

•	The ratings DataFrame
<img width="1287" alt="Screen Shot 2022-02-19 at 11 17 43 PM" src="https://user-images.githubusercontent.com/72629108/154831175-226942c4-c329-4381-8fa2-2083b797e43c.png">



### Extract and transform the Wikipedia Data

Using the knowledge of Python, Pandas, the ETL process, and code refactoring, extract and transform the Wikipedia data so we can merge it with the Kaggle metadata. While extracting the IMDb IDs using a regular expression string and dropping duplicates, use a try-except block to catch errors.


Cleaned wiki_movies_df DataFrame 

<img width="1337" alt="Screen Shot 2022-02-19 at 11 20 11 PM" src="https://user-images.githubusercontent.com/72629108/154831221-1a9e4ff9-512c-4e99-a663-4c7aad0c638c.png">


The columns from wiki_movies_df DataFrame to a list,
<img width="1337" alt="Screen Shot 2022-02-19 at 11 20 26 PM" src="https://user-images.githubusercontent.com/72629108/154831238-e98bf847-7fab-41a7-a0e0-6e747c85e7ce.png">



### Extract and Transform the Kaggle Data
Here we refactored the code  to extract and transform the Kaggle metadata and MovieLens rating data, then convert the transformed data into separate DataFrames. Then, merge the Kaggle metadata DataFrame with the Wikipedia movies DataFrame to create the movies_df DataFrame. Finally, merge the MovieLens rating data DataFrame with the movies_df DataFrame to create the movies_with_ratings_df

Movies_df DataFrame (after merging kaggle and wiki dataframes)
<img width="1337" alt="Screen Shot 2022-02-19 at 11 22 17 PM" src="https://user-images.githubusercontent.com/72629108/154831335-72e95aff-9820-478f-98a3-265e665b30ec.png">

Movies with ratings_df
<img width="1337" alt="Screen Shot 2022-02-19 at 11 22 08 PM" src="https://user-images.githubusercontent.com/72629108/154831349-aef6b14d-86d9-4a85-a3fc-9f172711d2b0.png">



### Create the Movie Database
In Deliverable #4 we establish  a connection with PostgreSQL and load the movies_df DataFrame and MovieLens rating CSV data to a SQL database.
## Results
We successfully created ETL pipeline to extract data then transform and load data to the database.

## Tools
•	PostgreSQL 11- Database
•	Jupyter notebook
•	Software: Python 3.7.9


