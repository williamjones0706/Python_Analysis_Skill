# Python Analysis Skills

This repo contains 3 parts, each uses python language/libraries to perform the tasks below:

Part I: Contains a series of different python techniques to print user selections, store selected data in new files, reformat and append data to create new information, and analyze data for key takeaways.

Part II: Analyze financial records and automate voting outcome results.

Part III: Reformat a large number of employee records and automate text analysis.

#------------------------------------------------------------------------------------
#------------------------------------------------------------------------------------

# Part I:

# House of Pies user selection: 
Create an order form that will display a list of pies to the user in the following way:
Welcome to the House of Pies! Here are our pies:
---------------------------------------------------------------------
(1) Pecan, (2) Apple Crisp, (3) Bean, (4) Banoffee,  (5) Black Bun, (6) Blueberry, (7) Buko, (8) Burek,  (9) Tamale, (10) Steak
Then prompt the user to select which pie they'd like to order via number.
Immediately after, follow the order with Great! We'll have that <PIE NAME> right out for you. and then ask if they would like to make another order. If so, repeat the process.

# Udemy data conversion: 
Create a Python application that reads the data on Udemy Web Development offerings.
Then store the contents of the Title, Price, Subscriber Count, Number of Reviews, and Course Length into Python Lists.
ADDITIONAL STEP: Find the percent of subscribers that have also left a review on the course. Include this in your final output.
ADDITIONAL STEP: Parse the string associated with course length, such that we store it as an integer instead of a string. (i.e. "4 hours" should be converted to 4).
Then zip these lists together into a single tuple.
Finally, write the contents of your extracted data into a CSV. Make sure to include the titles of these columns in your csv.

# Generate emails for employees:
Use csv.DictReader to read the contents of a csv file into a dictionary.
Use the first_name and last_name keys to create a new email address using the first and last name of the employee. {"first_name": "John", "last_name": "Glenn"} would generate the email: john.glenn@example.com.
Create a new dictionary that includes the first_name, last_name, ssn, and email.
Append the new dictionary to a list called new_employee_data.
Use csv.DictWriter to output the new_employee_data to a new csv file.

# Analyze resumes
Read the resume file as text using the with statement.
Create a list containing all words in the resume.
Convert each word to lowercase to normalize the data.
Use split to remove and trailing punctuation so only words remain.
Create a set of unique words from the resume using set().
Use set operations to filter out all remaining punctuation from the set of words.
Create a set from string.punctuation to use in the difference operation.
Use the cleaned set (no punctuation) to find all of the words from the resume that match the required skills.
Use the cleaned set (no punctuation) to find all of the words that match the desired skills.
Count the number of occurrences for each word in the resume and print the top 10 occurring words in the resume.
Use a dictionary data structure to hold the counts for each word.
Make sure to remove punctuation and stop words

#------------------------------------------------------------------------------------
#------------------------------------------------------------------------------------

# Part II:
#  Pybank
In this challenge, you are tasked with creating a Python script for analyzing the financial records of your company. You will give a set of financial data called budget_data.csv. The dataset is composed of two columns: Date and Profit/Losses. (Thankfully, your company has rather lax standards for accounting so the records are simple.)

Your task is to create a Python script that analyzes the records to calculate each of the following:
The total number of months included in the dataset
The net total amount of "Profit/Losses" over the entire period
The average of the changes in "Profit/Losses" over the entire period
The greatest increase in profits (date and amount) over the entire period
The greatest decrease in losses (date and amount) over the entire period

# Pypoll
In this challenge, you are tasked with helping a small, rural town modernize its vote-counting process. (Up until now, Uncle Cleetus had been trustfully tallying them one-by-one, but unfortunately, his concentration isn't what it used to be.)
You will be give a set of poll data called election_data.csv. The dataset is composed of three columns: Voter ID, County, and Candidate. Your task is to create a Python script that analyzes the votes and calculates each of the following:

The total number of votes cast
A complete list of candidates who received votes
The percentage of votes each candidate won
The total number of votes each candidate won
The winner of the election based on popular vote.

#------------------------------------------------------------------------------------
#------------------------------------------------------------------------------------

# Part III:

# Employee record reformatting
You oversee hundreds of employees across the country developing Tuna 2.0, a world-changing snack food based on canned tuna fish. Alas, being the boss isn't all fun, games, and self-adulation. The company recently decided to purchase a new HR system, and unfortunately for you, the new system requires employee records be stored completely differently.
Your task is to help bridge the gap by creating a Python script able to convert your employee records to the required format. Your script will need to do the following:

Import the employee_data.csv file, which currently holds employee records like the below:

Emp ID,Name,DOB,SSN,State
214,Sarah Simpson,1985-12-04,282-01-8166,Florida
15,Samantha Lara,1993-09-08,848-80-7526,Colorado
411,Stacy Charles,1957-12-20,658-75-8526,Pennsylvania

Then convert and export the data to use the following format instead:

Emp ID,First Name,Last Name,DOB,SSN,State
214,Sarah,Simpson,12/04/1985,***-**-8166,FL
15,Samantha,Lara,09/08/1993,***-**-7526,CO
411,Stacy,Charles,12/20/1957,***-**-8526,PA

# Automate text analysis
Create a Python script to automate the analysis of any such passage using these metrics. Your script will need to do the following:

Import a text file filled with a paragraph of your choosing.

Assess the passage for each of the following:

Approximate word count
Approximate sentence count
Approximate letter count (per word)
Average sentence length (in words)

As an example, this passage:

“Adam Wayne, the conqueror, with his face flung back and his mane like a lion's, stood with his great sword point upwards, the red raiment of his office flapping around him like the red wings of an archangel. And the King saw, he knew not how, something new and overwhelming. The great green trees and the great red robes swung together in the wind. The preposterous masquerade, born of his own mockery, towered over him and embraced the world. This was the normal, this was sanity, this was nature, and he himself, with his rationality, and his detachment and his black frock-coat, he was the exception and the accident a blot of black upon a world of crimson and gold.”

...would yield these results:
Paragraph Analysis
-----------------
Approximate Word Count: 120
Approximate Sentence Count: 5
Average Letter Count: 4.6
Average Sentence Length: 24.0


