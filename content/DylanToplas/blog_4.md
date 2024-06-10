---
title: "Dylan's Third Article"
date: 2024-06-10
draft: false
description: "Progress Report Week 4"
slug: "fourth"   # if you use, needs to be different for every post
tags: ["authors", "config", "docs"]
authors:
  - "dylan_toplas"
showAuthorsBadges : false
---

# Week 4, Project Update

Where do I even start... 

Thank you Dr. Fontenot and Dr. Gerber for a month that we'll rememeber forever. 

My main contribuition this week was gathering the stock data that was used in the LSTM and stock search features in our app. I first had to get politicians' orders data with Andrew, load it into a Jupyter Notebook as a list, and searched every item in the list in yfinance and download its corresponding 3 year data. Afterwards, I had to create columns for ticker and company and download the resulting dataframe as a csv and input that csv into a script to get SQL "insert" statements for each data entry. I spend a ridicously large amount of time debugging the insert statements but I managed to prevail at the end. It was a challenging last night to finish the project but working as a team at 2am with every group working hard to improve their project was truly inspirational. 

I also contribuited to add dropdowns for stock and politician searches so that the app's user could view their search options in real time before selecting the desired result. Joshua and I worked together to implement database changes so that the new features worked flawlessly. 

Once we got the stock data, Andrew, Ramsey, and me worked on fixing the stock search functionality and displaying the stock's closing values in the stock detail page. The data was not ordered so we fixed that and printed the last 90 days of stock market data. 

In terms of presentations and travel, this week was extremely fun, specially the C-Mine and Thor Park presentations. I also really enjoyed going to Brussels and working on that cafe. 
