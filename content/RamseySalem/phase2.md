---
title: "Ramsey's Second Phase Blog Post"
date: 2024-05-28
draft: false
description: "Second Phase Progress"
slug: "second"   # if you use, needs to be different for every post
tags: ["authors", "config", "docs"]
authors:
  - "ramsey_salem"
showAuthorsBadges : false
---

There were originally some issues when I started the data collection for the project. The idea of simply tracking stocks did not offer any functionality. I proposed we create a trading simulation with fake money for users to see how their money grows, along with saving stocks and top political figures trades. When I came up with the idea of the stock prediction based off politician's trades, there was missing data. I was on the train and started to work on the API implementation of Financial Modeling Prep, and a lot of the data seemed to be restricted due to it needing a subscription. I went on searching more and found a website where we would scrape called capitoltrades.com. Andy had taken up scraping and grabbing the data of politicians that fit the filters I created. The trade must be over $50,000 and divided between US and international stocks. I also switched to using the yahoo finance API for financial statements and data so that we could create an ML model. I plotted the data with candlesticks so that users could see the highs and lows of the data for each day, representing an actual stock graph over a course of 3 years. I also implemented the linear regression model, but I mixed up the X and Y’s on one of the functions, and Andy helped me fix it. I also tried to get the data for recent legislation so we can create a relevant legislation page in the app, where users can see on the graph in the months what legislation has been passed along with what politicians invested in different stocks. 