# Credit Card Fraud Analysis
Project_1_Group_3

Classmates in Group 3 are:
Cory Lingerfelt,
Gregory Smith,
Kelly Carter,
Sara Kleine-Kracht,

# Project Overview

In this project, we analyzed fraudulent credit card transaction data to measure the level of impact across various parameters. The goal was to identify patterns that can support preventative action planning. 

# Description of the Data

We merged two simulated csv datasets of fraudulent credit card transactions. The merged dataset had close to 500,000 entries so we pulled a random sample of 10,000 transactions to analyze. We cleaned the data and removed unneccesary columns. We converted the base dataframe of the cleaned sample data to a csv which was utilized in each team members' code to ensure we were all using the same sample. 

The columns we performed our analysis on are:

  Trans_date_trans_time: Displays the date and time of the transaction
  
  Category: The transaction category (gas and transport, home, entertainment, etc.)
  
  Amt: The total amount (in USD) of the transaction
  
  Gender: The gender (M/F) of the victim
  
  City: The city where the transaction occurred
  
  State: The state where the transaction occurred
  
  Lat: The latitude where the transaction occurred
  
  Long: The longitude where the transaction occurred
  
  City_pop: The population of the city where the transaction occurred
  
  Dob: The date of birth of the victim
  
  Merch_lat: The latitude where the fraudulent merchant is located
  
  Merch_long: the longitude where the fraudulent merchant is located

# Research Questions

How does geography affect fraudulent transactions?

How does victim demographic impact the frequency of fraudulent transactions?

How is the frequency of fraudulent transactions impacted by merchant category?

How does timing impact frequency of fraudulent transactions?

# Communication Protocols

In order to update each other on the status of our individual parts of the project we established frequent communication through Slack and Zoom meetings.

# Data Tools Used

We used jupyter notebook, pandas, and python libraries to clean, analyze, and visualize the data. 

# Results

How does geography affect fraudulent transactions?

How does victim demographic impact the frequency of fraudulent transactions?

How is the frequency of fraudulent transactions impacted by merchant category?

When analyzing the category types from the fraud dataset, we wanted to find the category that had the highest number of fraudulent transactions and which category accounted for the highest amount of loss
Gas and Transport was the merchant category with the highest frequency of fraudulent credit card transactions. Travel was the merchant category with the lowest frequency of fraudulent credit card transactions. The Grocery (In Store) category accounted for the highest dollar amount lost through fraudulent transactions with $107,104.88. The Grocery (Online) category had the lowest total loss in dollars with $18,965.07.


How does timing impact frequency of fraudulent transactions?


# Presentation Link

The link to the slide deck is: 



