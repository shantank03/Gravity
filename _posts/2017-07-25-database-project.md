---
layout: post
title: "Gathering Data and Compiling it into a MySQL database"
date: 2017-07-25 16:30:00
category: ["data"]
author: Shantan Krovvidi
---
# Abstract
The purpose of this project is to learn how to continuously gather data using a script and then input that data into a SQL database for future use/querying.
I really like this script because it allows for the database to be considered live as it continuously aggregates data as it is entered by the user.

## Data Collection Script
Labelled as "data-handling.sh" this script outputs five survey questions and the user can input answers to these questions.
The script reads these responses as variables and stores them into a master CSV file.
Beyond these variables, the script calls a unique identifier for each observation/user and generates a timestamp for whenever the script is run.

## SQL Database Creation Script
Labelled as "write-to-db.sh" this script inputs the data gathered in the first script to a database in MySQL.
In the script, I am able to call the username and password in variables and the script can automatically go into SQL to create and edit a database and tables.
Using conditional statements, I create the table and database based on whether or not there are tables or databases with the names that I am using.
Once the script has run past the creation phase, it will automatically load any new data into the table as data is entered live as the first script is called.
Finally, the database is dumped into a .sql file.

[Link to GitHub Repository to access scripts and data files](https://github.com/shantank03/data-handling-assignment)
