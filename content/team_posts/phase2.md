---
title: "Project - Phase 2"
date: 2024-05-28
draft: false
description: "Our Idea"
slug: "phase2post"
tags: ["authors", "config", "docs"]
authors:
  - "joshua_segal"
  - "andy_sun"
  - "dylan_toplas"
  - "ramsey_salem"
showAuthorsBadges : false
---

# Phase 2 CS 4973 Group 4

## Database 

To support our goal of building the application in an organized manner, a comprehensive entity-relationship diagram was constructed. We initially had some trouble understanding what made each user persona unique, and overcame this obstacle through adding advanced features for each user such as: paper trading for our investor persona, legislation tracking for our journalist persona, and politician watchlists for political managers. In order to increase database look-up speeds and decrease data redundancy, we incorporated best-practice rules for:
- Strong entity types
- Weak entity types
- 1:1 relationships
- 1:M relationships
- M:N relationships
- Multivalued attributes


<img src="https://i.imgur.com/bpkJ9rb.png">
<class="center"/>

## Wireframes PoC

Afterwards, we develop Wireframes of Proof of Concept models for each user persona to better visualize similarities and differences of the unique user experiences. This further adds to the organized nature of our approach in building this application while maintaining the different utilities that we initially planned for our project. We focused on the three main uses for each persona to better display what the interactive features would be for each one, as well as identifying the uniqueness of each case. The concepts can be seen below:

<img src="https://i.imgur.com/pQtS9nP.png"> 
<class="center"/>

## SQL DDL

The next step was to convert our ER diagram into a database schema in MySQL. Key considerations included fulfilling the different relationship types, and effectively establishing data types.

<img src="https://i.imgur.com/83xUkcC.png">
<class="center"/>

## Data Collection 

The purpose of our project is to project future stock prices on stocks that have been recently purchased by major politicians. One of the dataset we were able to obtain was a website that had all of the information we needed (https://www.capitoltrades.com/), and we would need to do some web scraping to be able to transform the data into a usable format. We initially encountered some issue collecting the data as all of the html code regardless of page were the same. After some help with the professors, we were able to successfully gather the data through web scraping.

We found a second data source, Yahoo Finance API (yfinance), to gather more detailed information on a specific stock ticker(based on the stock tickers we observed with the first dataset). This is when we can use the historical stock data like volume and price to plot a time-series visualization and discover any possible linear trends. 

<img src="https://i.imgur.com/e5JsUks.png">
<class="center"/>

<img src="https://imgur.com/a/uPVYOR5.png">
<class="center"/>

## Visualization 

Our first visualization showcases a certain stock’s price over a period of time(3 years for this visualization). The plotly library has a cool Candlestick feature that allows the viewer to see when a stock price increases or decreases based on color. We then implemented a line of best fit on the stock prices to determine if we could demonstrate a trend or correlation between the two variables of stock price and date. For example, using a line_of_best_fit function, we concluded that the equation of the linear regression of the stock of Apple was y = 1.42741982e+02, 5.36644130e-02x. The y-intercept of 142.74 indicates that exactly 3 years before, the stock price is projected to be $142.72. The slope of 0.05366 means that the stock price is projected to increase by $0.05 per share everytime 1 day passes.

However, even with this analysis, we could tell that there really wasn’t a clear linear pattern as the prices seemed to fluctuate frequently. We calculated a r2 score of 0.44, not too good, and could definitely be improved. As of now, we’re not too sure which feature would be better to use for a linear regression, but at least we have something to base off our r2 score of. Our next step is to find a second ML model we could implement in our analysis to make further conclusions with the dataset.

<img src="https://i.imgur.com/tuzp6Af.png">
<class="center"/>