---
title: "Project - Phase 4"
date: 2024-06-10
draft: false
description: "Finishing Touches"
slug: "phase4post"
tags: ["authors", "config", "docs"]
authors:
  - "joshua_segal"
  - "andy_sun"
  - "dylan_toplas"
  - "ramsey_salem"
showAuthorsBadges : true
---

# Phase 4 CS 4973 Group 4

For phase 4 of our project, the team worked relentlessly to present the final version of the project. Most of the work was refining the machine learning model and making the application functionalities with real data. Below is a more detailed description of each step: 

## Machine Learning

For our first machine learning model, we utilized a simple linear regression model used to predict the volume of stocks traded per politician based on the date. While we are aware that using a time-series model isn't the best feature to use for a linear regression. The reason is because a linear regression model assumes that the x-values are independent, however a time-series data will have the date points that are typically dependent on their previous values. Regardless, with limited available information using web scraping, using date as the x-feature was the next best option to use. How we implemented the model into streamlit was we first had to create a politician_trade_volume route which queries the politician_stock database based on a certain name and group by the total values of each stock being purchased or sold. Once we got the requests successfully, we were then able to apply the linear regression functions and return a vector that returns a slope and a intercept. With these two information, we were then able to create an equation that could be used to calculate all of the y predicted values and use that to plot with the trade volume in streamlit.

For our second machine learning model, we chose to implement a Long Short-Term Memory model to predict future stock performance after a politician has bought/sold a stock. This model took a lot of time, considering it is a subset of a recurrent neural network, we never had time to cover this in class, so it was all self taught. Although it is fully implemented into our website, still we all do not have a complete understanding of how the layers or the network interact with data. The model was made to predict the stock price, specifically stocks after they were bought/sold after a politician made a trade on specific stocks. This would show how there is a potential for insider trading due to the prediction and the amount of a stock bought at a certain time. 

<img src="https://i.imgur.com/Ps7mWMz.png">
First ML model

## Gathering Real Data

To gather real data, we used web scraping of this website (https://www.capitoltrades.com/) to gather politicians' orders. From those stocks, Yfinance was used to get the last 3 years data for each. We then downloaded the dataframe as a csv and used a program to write the “insert” statements. We also grabbed a csv file from congress.gov, and cleaned the data and made it into a new csv file. This csv file had data on all past bills that were passed, and what congress person sponsored that bill. This data is displayed in the stock detail page and it is used to train the machine learning models. The last step was to gather real legislation data from Kaggle as the official government website did not allow for web scrapping. 

In gathering this data we faced both compute time and storage capacity constraints. In order to mitigate this we further seperated our tables to reduce complexity of individual queries.

<img src="https://i.imgur.com/tPMWaa8.png">
Final SQL Database

## Overall Software Architecture
Overall, our app was successfully able to have both the front and back end communicate with each other using routes that we built in our code. With the requests, we were either able to GET, POST, UPDATE, or DELETE from the selected database table and have the changes been seen on Streamlit. 

## Tech Stack

### Streamlit 
Streamlit served as the front-end framework, enabling quick development of interactive dashboards. Its simple, Pythonic API allowed us to quickly build a full-stack web applications, handling real-time data updates.

### Flask 
Flask was used to build the backend, providing a lightweight and flexible framework. Flask allowed us to implement RESTful endpoints and integrate seamlessly with the Streamlit front-end and MySQL database.

### Docker
Docker's containerization technology encapsulated our application and its dependencies, guaranteeing identical performance regardless of the underlying infrastructure. This setup facilitated easy deployment and scaling of the application.

### MySQL
MySQL was our data storage tool. Its relational database system provided reliable and efficient querying capabilities.

Together, these technologies created a cohesive and efficient architecture for our CS4973 project, combining interactive visualization, flexible web services, consistent deployment, and reliable data management.

## Improving User Interface

To improve the design of our app and make it more unique, we implemented dropdowns instead of a search box as we had in the last phase. This provides a more modern look in the search and ensures that the user views their search results in real time before making a decision. Additionally, a brief description of each user persona's needs for the app was added in the home page for clarification. 

<img src="https://i.imgur.com/OhcbNzX.png">
Home Page

<img src="https://i.imgur.com/lZiGMSW.png">
Politician Search

<img src="https://i.imgur.com/ybreyQY.png">
Legislations Info

## Final Thoughts

To present the utilities of the application, we created a slides show to support our 30 minutes presentation that happened on Monday, June 10 2024 on our last day of the dialogue. The team thanks you for the engagement and we hope you enjoy using the application.

## Link to Presentation
https://docs.google.com/presentation/d/1hv6pK8exUZkUF5u43LQW8GSZbZ8jVukbYMO3Q2gwlnU/edit?pli=1#slide=id.g2e489ec6cba_1_51