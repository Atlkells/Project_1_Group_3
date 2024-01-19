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

fraudTest.csv was sourced from Kaggle and is a simulated credit card transaction dataset containing fraudulent transactions from the duration 1st Jan 2019 - 31st Dec 2020. It covers credit cards of 1000 customers doing transactions with a pool of 800 merchants. This was generated using Sparkov Data Generation | Github tool created by Brandon Harris. (https://www.kaggle.com/datasets/kartik2112/fraud-detection). It contains 



We merged the datasets using "outer" and on the columns below:

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

When we looked at a heat map of the locations of fraudulent transactions, it looked like most of them were centered around the more populated parts of the country with large blank spots over the upper and western plains areas and more desertous regions of the West, and more concentrated areas in places like California and the eastern United States. There doesn't seem to be any specific populated areas that stand out as being more targeted than other populated areas.

<img width="365" alt="image" src="https://github.com/Atlkells/Project_1_Group_3/assets/148706472/625a3281-85c3-4a30-8455-920a18f81ef4">


This also lines up with the maps of where the fraud victims live. Again we see a similar pattern of blank areas being focused in the nothern and western plains areas as well as around the deserts in the Southwest of the country. Again there doesn't seem to be a populated region that is more concentrated than other populated areas of the map. 

<img width="290" alt="image" src="https://github.com/Atlkells/Project_1_Group_3/assets/148706472/a53083f8-cb15-44e8-8ffd-bd44800e0b9b">


One of the other items we were interested in looking at was the way population size would affect the size of the transactions. To investigate this we ran a scatter plot of the two variables to attempt to determine correlation between the two. There was no discernable positive or negative correlation. The linear regression gave us a positive of 0.1. There were some outliers in the fraudulent transaction amount with most transactions being below the $1,500 amount, but there were some transactions above $3,500 and $4,000 all occuring in populations below 500,000 people. The majority of fradulent transactions were in amounts less than $1,500 in cities with less than 1,000,000 people. This makes sense given that there are only ten cities in the US with population above 1,000,000. This coupled with the two maps previously mentioned does seem to support a conclusion that the location and population does not seem to affect the amount of money fraudulent transactions go for or the frequency of fraudulent transactions.

<img width="484" alt="image" src="https://github.com/Atlkells/Project_1_Group_3/assets/148706472/e495dded-ae9b-4c1d-9aec-53791799425d">


How does victim demographic impact the frequency of fraudulent transactions?

The first demographic we looked at was the breakdown percentages of Male and Female victims in our sample. We found that 55.8% of our fraud victims were female, and 44.2% of our victims were Male. According to the US Census, 50.4% of the US population is female. This is a statistically significant differnce, but more research would need to be done into why the percentage is higher. Some possible variables that could be causing this that aren't part of our data set are if women are more active shoppers than men in general, if they shop at the categories that have a higher frequency of fraud, or if they tend to have more credit cards or not.

<img width="293" alt="image" src="https://github.com/Atlkells/Project_1_Group_3/assets/148706472/6b3749a7-87b3-40de-b12e-a36ec69c6f89">


One of the prevalent assumptions that exists is that older people are mroe likely to be victims of fraud than people who are younger. There are two prevalent reasons behind this such as the assumption that older people have had more time to build good credit scores and better limits, and the assumption that older people are less in touch with newer technology than younger generations. After we divided the data into generations, we looked at the frequency of fraudulent transactions by generation. This returned a histogram that looked more or less like a bell curve with Gen X and Millenials having the highest number of fraudulent transactions.

<img width="415" alt="image" src="https://github.com/Atlkells/Project_1_Group_3/assets/148706472/0b638309-95e2-48c2-afa2-073d68056c92">

Looking at the counts of fraudulent transaction for each generation--the Silent Generation had 824 accounting for 8.24% of the sample, the Baby Boomer generation had 1,898 accounting for 18.98% of the sample, Generation X had 3,324 accounting for 33.24% of the sample, Millenials had 3,223 accounting for 32.23% of the sample, and Generation Z had 662 accounting for 6.62% of the population. According to the US Census the percent of the US population that each generation makes up is as follows -- Silent Generation - 5.49%, Baby Boomer Generation - 20.58%, Generation X - 29.61%, Millenials - 21.67%, and Generation Z - 20.88%. Looking at the percentages in our sample, the Baby Boomer Generation and the Millenial Generation make up a much bigger percentage of fraud cases than they do the US population. This would seem to indicate that the earlier assumptions are wrong; however there could be other variables at play given that not all members of Generation Z are old enough to have credit cards.

We further looked at the relationship between age and transaction amount to see if there was any relationship between which transactions had the highest dollar amount and age of the victim. When we looked at the correlation, we again found that there was no discernable positive or negative correlation between the two.

<img width="434" alt="image" src="https://github.com/Atlkells/Project_1_Group_3/assets/148706472/3d05fcf2-c9fe-4af7-98e0-94939fb19a2d">

How is the frequency of fraudulent transactions impacted by merchant category?

When analyzing the category types from the fraud dataset, we wanted to find the category that had the highest number of fraudulent transactions and which category accounted for the highest amount of loss
Gas and Transport was the merchant category with the highest frequency of fraudulent credit card transactions. Travel was the merchant category with the lowest frequency of fraudulent credit card transactions. The Grocery (In Store) category accounted for the highest dollar amount lost through fraudulent transactions with $107,104.88. The Grocery (Online) category had the lowest total loss in dollars with $18,965.07.

<img width="139" alt="image" src="https://github.com/Atlkells/Project_1_Group_3/assets/148706472/0d249000-3307-4862-8007-65db84e51ecc">

<img width="592" alt="image" src="https://github.com/Atlkells/Project_1_Group_3/assets/148706472/63a6d22c-16cf-4c66-ba97-4bbbd908e1c9">

<img width="182" alt="image" src="https://github.com/Atlkells/Project_1_Group_3/assets/148706472/9f224e85-94f8-41ae-a245-83d6d20aa51d">

<img width="582" alt="image" src="https://github.com/Atlkells/Project_1_Group_3/assets/148706472/5cba9ff3-f899-4ae5-9d93-1c5bb2b94c9a">




How does timing impact frequency of fraudulent transactions?

The final question we looked at is how does timing impact the frequency of fraudulent transactions. We specifically looked at the frequency of fraudulent transactions over different months and time of day.

<img width="438" alt="image" src="https://github.com/Atlkells/Project_1_Group_3/assets/148706472/269ee363-a57b-4ecb-92e3-f627786167aa">

When looking at the different months of the year, there is a much higher frequency of fraudulent transactions in December than in any of the other months. There are over 2,000 fraudulent transactions in the month of December while the next closest month, August, has less than 1500. This would seem to line up with two of the biggest shopping times of the year with December bringing Christmas, and August being the back to school shopping time. 

<img width="433" alt="image" src="https://github.com/Atlkells/Project_1_Group_3/assets/148706472/d5d427f9-a38c-4dac-bbed-61bf5cd2f613">

Looking at the time of day, more transactions happen in the afternoon and evening than in the morning. The graph is using military time markers, so 00 is midnight. The biggets spikes in fraudulent transactions are from 12-1pm and from 7 to 8 pm, but the entire afternoon is above 400 fraudulent transactions while the entire morning is below 400 fraudulent transactions. More data would need to be compiled and more research done to explain why this happens to be the case. Are fraudsters late-risers? Do they do more activity over lunch breaks and dinner rushes because they are working regular jobs the rest of the time? Is it just that these are the times of day more people are active?

Our analysis is just scratching the surface of credit card fraud, but the discrepency between generation population percentages and fraud percentages, sex and fraud percentages, and time of day fraud frequency are all areas that we would view as beneficial to look further into were we working for a credit card company trying to combat fraud.


# Presentation Link

The link to the slide deck is: https://docs.google.com/presentation/d/1yHLMCYSU1Mfhi1vYFxGED0zgqLm35ZsSChHIjSObYrk/edit#slide=id.p3



