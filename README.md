# NoSQL Challenge: UK Food Standards Agency Data Analysis

## Before You Begin
Create a new repository for this project called nosql-challenge. Do not add this homework to an existing repository.

Clone the new repository to your computer.

Add your Jupyter notebook starter files and your Resources folder containing establishments.json to this folder.

Push the changes to GitHub.

Files
Download the following files to help you get started:
- [Module 12 Challenge files](https://static.bc-edx.com/data/dl-1-2/m12/lms/starter/Starter_Code.zip)

## Instructions

### Part 1: Database and Jupyter Notebook Set Up
Use NoSQL_setup_starter.ipynb for this section of the challenge.

1. Import the data provided in the establishments.json file from your Terminal. Name the database uk_food and the collection establishments. Copy the text you used to import your data from your Terminal to a markdown cell in your notebook.

2. Within your notebook, import the libraries you need: PyMongo and Pretty Print (pprint).

3. Create an instance of the Mongo Client.

4. Confirm that you created the database and loaded the data properly:
   - List the databases you have in MongoDB. Confirm that uk_food is listed.
   - List the collection(s) in the database to ensure that establishments is there.
   - Find and display one document in the establishments collection using find_one and display with pprint.
   - Assign the establishments collection to a variable to prepare the collection for use.

### Part 2: Update the Database
Use NoSQL_setup_starter.ipynb for this section of the challenge.

1. Add an exciting new halal restaurant just opened in Greenwich, but hasn't been rated yet. Update the database accordingly.

2. Find the BusinessTypeID for "Restaurant/Cafe/Canteen" and return only the BusinessTypeID and BusinessType fields.

3. Update the new restaurant with the BusinessTypeID you found.

4. Remove any establishments within the Dover Local Authority from the database.

5. Convert number values stored as strings to numbers.

### Part 3: Exploratory Analysis
Use NoSQL_analysis_starter.ipynb for this section of the challenge.

1. Answer specific questions using MongoDB queries:
   - Which establishments have a hygiene score equal to 20?
   - Which establishments in London have a RatingValue greater than or equal to 4?
   - What are the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
   - How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest, and print out the top ten local authority areas.

## Requirements

### Part 1: Database and Jupyter Notebook Set Up (15 points)
- Include the mongoimport command text you used to import establishments.json in a markdown cell at the beginning of your Jupyter notebook file.
- The mongoimport command text correctly drops any existing establishments collection before importing establishments.json into MongoDB.
- The database is named uk_food and the collection is named establishments.
- Correctly imports PyMongo and Pretty Print.
- An instance of the Mongo Client is created.
- Lists the databases you have in Mongo, which includes uk_food.
- Lists the collection(s) in the uk_food database, which includes establishments in the output.
- Uses find_one() and pprint to display one document in the establishments collection.
- The establishments collection is assigned to a variable.

### Part 2: Update the Database (20 points)
- The supplied data for the "Penang Flavours" restaurant is correctly inserted into the establishments collection.
- A query is performed to find the BusinessTypeID for "Restaurant/Cafe/Canteen" and returns only the BusinessTypeID and BusinessType fields.
- The "Penang Flavours" document is updated with the correct value for BusinessTypeID.
- A query is correctly performed to delete all the documents in the collection where "Dover Local Authority" is the value for LocalAuthorityName.
- A count_documents() check is performed before and after the removal of the Dover documents to ensure the documents were removed.
- An update_many() query is performed to convert the latitude and longitude fields from strings to decimal numbers and RatingValue to integers.

### Part 3: Exploratory Analysis (55 points)
- Questions 1-4 are answered correctly using MongoDB queries.
- For each question:
  - A query is correctly performed to find the required information.
  - count_documents() is used to list the correct number of documents.
  - The first result is printed using pprint.
  - The results are converted to a Pandas DataFrame and displayed.

## Deployment and Submission (6 points)
- Submit a link to a GitHub repository that’s cloned to your local machine and contains your files.
- Use the command line to add your files to the repository.
- Include appropriate commit messages in your files.

## Comments (4 points)
- Be well commented with concise, relevant notes that other developers can understand.

## Grading
This assignment will be evaluated against the requirements and assigned a grade according to the following table:

Grade	Points
A (+/-)	90+
B (+/-)	80–89
C (+/-)	70–79
D (+/-)	60–69
F (+/-)	< 60

## Submission
As a reminder, the deliverables for this Challenge are as follows:

Deliverable 1: A Jupyter notebook containing code that imports the data and sets up and updates the uk_food database.

Deliverable 2: A Jupyter notebook containing code that performs the exploratory analysis queries in the database.

To submit your Challenge assignment, click Submit, and then provide the URL of your GitHub repository for grading.
