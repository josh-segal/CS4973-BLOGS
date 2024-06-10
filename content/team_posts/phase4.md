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

For our second machine learning model, we chose to implement a Long Short-Term Memory model to predict future stock performance after a politician has bought/sold a stock. This model took a lot of time, considering it is a subset of a recurrent neural network, we never had time to cover this in class, so it was all self taught. Although it is fully implemented into our website, still we all do not have a complete understanding of how the layers or the network interact with data. The model was made to predict the stock price, specifically stocks after they were bought/sold after a politician made a trade on specific stocks. This would show how there is a potential for insider trading due to the prediction and the amount of a stock bought at a certain time.

## Gathering Real Data

To gather real data, we used web scraping of this website (https://www.capitoltrades.com/) to gather politicians' orders. From those stocks, Yfinance was used to get the last 3 years data for each. We then downloaded the dataframe as a csv and used a program to write the “insert” statements. We also grabbed a csv file from congress.gov, and cleaned the data and made it into a new csv file. This csv file had data on all past bills that were passed, and what congress person sponsored that bill. This data is displayed in the stock detail page and it is used to train the machine learning models. The last step was to gather real legislation data from Kaggle as the official government website did not allow for web scrapping. 

## Improving User Interface

To improve the design of our app and make it more unique, we implemented dropdowns instead of a search box as we had in the last phase. This provides a more modern look in the search and ensures that the user views their search results in real time before making a decision. Additionally, a brief description of each user persona's needs for the app was added in the home page for clarification. 

## Final Thoughts

To present the utilities of the application, we created a slides show to support our 30 minutes presentation that happened on Monday, June 10 2024 on our last day of the dialogue. The team thanks you for the engagement and we hope you enjoy using the application.

## Link to Presentation
https://docs.google.com/presentation/d/1hv6pK8exUZkUF5u43LQW8GSZbZ8jVukbYMO3Q2gwlnU/edit?pli=1#slide=id.g2e489ec6cba_1_51