---
title: "Project - Phase 3"
date: 2024-06-06
draft: false
description: "Implementing"
slug: "phase3post"
tags: ["authors", "config", "docs"]
authors:
  - "joshua_segal"
  - "andy_sun"
  - "dylan_toplas"
  - "ramsey_salem"
showAuthorsBadges : true
---

# Phase 3 CS 4973 Group 4

For this phase of the project, we were tasked with building the bulk of the application. On one side, our data science team worked on improving the machine learning model and creating a second model, while our database design team worked on improving the data model and implementing a RESTful API with flask, streamlit, and docker.

## Data Model

One of the strong points of the previous phase was the DDL and database design. This enabled us to keep the same data model as the last phase, but we did add data to the tables to have functioning features using fake data. We decided to solely use fake data to test that the features would be performing as expected with a small amount of data, and plan to connect our sourced data for the phase 4 kick-off.

## Gathering Data 
To insert data into our different user personas tables, Mockaroo was used in order to artificially create different profiles that would interact with the app. The tables used and their respective proposed data origin are as follows. However, all data was created with Mockaroo as of now.

- investor; generated 
- investor_order; generated
- investor_politician_order; generated
- investor_stock; generated
- journalist; generated
- journalist_legislation; generated
- journalist_politician; generated
- legislation; sourced
- legislation_politician_ids; sourced
- manager; generated
- politician; sourced
- politician_investor; sourced 
- politician_legislation; sourced
- politician_manager; generated
- politician_order; sourced
- politician_search_history; generated
- stock; sourced
- stock_search_history; generated

## Features of ML
As a team we decided to switch our approach to building the models. Originally we wanted the stock prediction to be a linear model, but we thought that using libraries such as sklearn and tensorflow would be more beneficial for the stock prediction portion of the website. The linear regression portion was decided to be the prediction of the volume of trades by politicians. This will show the amount of trading done by politicians, and also how much it has grown over quarterly or adjusted amounts of time. The main features of both ML’s so far is prediction, and where things may end up based on the given data that we trained the model with. The second model we chose for stock prediction was an LSTM model. We did some research and found that this was best for how a stock can be volatile and some stocks that aren’t. The LSTM model isn’t completed but it is very close to being finished.  

Throughout the model exploration process, we found how complex a simple linear regression model can be. One of the biggest challenges we encountered was determining if a linear regression model was even appropriate. For instance, when predicting the volume of stocks traded by politicians or a certain stock price over time, we found no distinct pattern, with values varying widely. This resulted in very low R² scores (~0.01-0.03).
To improve the model, we shortened the time frame from a few months, for example,(usually the users are able to adjust the dates) to one week over a couple of months. This change led to periods with a more consistent slope and higher R² scores. We found that this logic makes sense, because there are just too many variables, not just politicians that can influence stock prices, and so one idea we were able to conclude was that politicians' stock trades often have a short-term effect on stock prices.

<<<<<<< HEAD
## First Iteration of App

### Investor Persona
For the investor persona, some of the functionalities implemented were the ability to view stocks performance and track desireable stocks. The same functionality was done for politicians as seen below:

<img src="https://i.imgur.com/AJPwbzV.png"/>

 Date range and stocks will be controlled by the users.

<!-- <img src="https://i.imgur.com/fvgnif2.png"/> -->
<img src="https://i.imgur.com/MO6HyFY.png"/> 

The most searched stocks/politician are displayed before the search dropdown.

### Political Manager Persona
For the political manager persona, the functionalities added were the ablity to edit the manager profiles and the ability to search the politician like the investor persona

<img src="https://i.imgur.com/tuDt7bT.png">

## Machine Learning Model
As discussed above, the first machine learning model is a linear regression on stock performance after a key event (politician trade). The prediction is not a single line due to the exchange market being closed on weekends.

<img src="https://i.imgur.com/tajWstF.png"> 

In terms of calling the model in the application, we implemented that on the Journalist persona as seen below:
=======
<img src="https://imgur.com/XGiao41">
<class="center">
>>>>>>> e9ef791d4de4d9e97e494c51176033c5e405bc88
