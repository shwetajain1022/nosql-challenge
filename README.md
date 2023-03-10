# NoSQL Challenge
----
## Table of Contents

- Part 1: Database and Jupyter Notebook Set Up
- Part 2: Update the Database 
- Part 3: Exploratory Analysis

## Part 1: Database and Jupyter Notebook Set Up
--------------------------------------------------------------------------------------------
The work is stored in Jupyter Notebook file NoSQL_setup_starter.ipynb. Following are the steps below as specified:
1. Imported the data provided in the establishments.json file from your Terminal. command used : mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json
1. Imported the libraries PyMongo and Pretty Print.
1. Created an instance of the Mongo Client.
1. Performed the following checks on the MongoDB database
- Listed the databases in MongoDB and Confirmed that uk_food is listed.
- Listed the collection(s) in the database to ensure that establishments is there.
- Found and display one document in the establishments collection using find_one and display with pprint.
1. Assigned the establishments collection to a variable to prepare the collection for use.

## Part 2: Update the Database 
--------------------------------------------------------------------------------------------
All the coding was done in  Jupyter Notebook part_2_mars_weather.ipynb. Following are the steps below as specified:
1. New reaturant details "Penang Flavours" in json format inserted into establishments collection using insert_one().
1. Checked if the reaturant "Penang Flavours" was entered into the collection using MongoDB query find_one().
1. Found the BusinessTypeID to be 1 for "Restaurant/Cafe/Canteen" and return only the BusinessTypeID and BusinessType fields using MongoDB find query defining fields to be displayed.
1. Updated the new restaurant with the BusinessTypeID : 1 using update_one().
1. Found 994 documents that contain the Dover Local Authority using count_document(). 
1. Deleted any establishments within the Dover Local Authority from the database using delete_many()
1. Found 0 documents that contain the Dover Local Authority after deletion using count_document().
1. Updated the latitude and longitude from geocode to be double using update_many() .

## Part 3: Exploratory Analysis
--------------------------------------------------------------------------------------------
1. Which establishments have a hygiene score equal to 20?
Used query in find() function to put the condition for filtering of the results 
Answer - Total number of rows in the establishments with hygiene score 20 are 41
1. Which establishments in London have a RatingValue greater than or equal to 4?
Used regex condition for finding London Local Authority  
Answer - Total number of establishments with London as the Local Authority with RatingValue greater than or equal to 4 is 33
1. What are the top 5 establishments with a RatingValue of '5', sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
Used find(), sort(), limit() from pymongo library to get to the answer
Answer - Total number of establishments near by Penang Flavours restaurnat are 87
1. How many establishments in each Local Authority area have a hygiene score of 0? 
Used aggreate to find the answer below.
Answer - Total number of establishments near by Penang Flavours restaurnat are 87 

