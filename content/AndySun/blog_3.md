---
title: "Andy's Third Article"
date: 2024-06-05
draft: false
description: "hi!"
slug: "third"   
tags: ["authors", "config", "docs"]
authors:
  - "andy_sun"
showAuthorsBadges : false
---
# Week 3 Blog 

For phase 3, my main role  focused primarily on refining the first machine learning model(simple linear regression). I was able to implement two linear regression models: one to predict the volume of stocks traded on a specific date and another to predict stock prices after a certain politician either buy or sell stocks.

For predicting the total volume of stocks traded over a certain period, I initially had a very low R² score of around ~0.002. After analyzing for a while, I realized that this was most likely due to the lack of a clear linear pattern, as the total volume fluctuated significantly. As a result, I broke down the time frame into smaller sections, allowing for a clearer linear pattern and only focused on whenever the total volume either increased or decreased only. This change highlighted that a shorter time frame could reveal more consistent trends, making the linear regression model more effective(higher R^2 scores)

I came across a different issue for the stock price prediction model. The regression line wasn’t straight because stock prices only change during trading days (Monday-Friday). Over the weekends, the stock price remains constant, which disrupts the linearity of the regression. While it hasn't been fixed yet, I plan to adjust the model to account for the gaps by creating a new 'date column' based on the rows, ensuring that each day increase by one consistently.

Over the next few days, I plan to translate these mdoels into Streamlit. I am a bit anxious about the amount of work our group will have to do, but at least it will be 100% worth it at the end of the day. 

On a personal note, Belgium has been wonderful as always. Exploring Luxembourg’s this past weekend was also a refreshing and enjoyable experience. 


