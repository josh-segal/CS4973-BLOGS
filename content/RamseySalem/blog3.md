---
title: "Ramsey's Third Phase Blog Post"
date: 2024-06-06
draft: false
description: "Third Phase Progress"
slug: "third"   # if you use, needs to be different for every post
tags: ["authors", "config", "docs"]
authors:
  - "ramsey_salem"
showAuthorsBadges : false
---

Personal Blog for Phase 3:  

I first started brainstorming for phase 3, now having the task of doing another ML model, but the second one can be used with more resources, libraries, and more freedom. I came up with the idea that we could flip the models and have the stock prediction model be used with sckitlearn, tensorflow/keras. This would benefit us the most with our limited time, and linear regression would be tough to get accurate with stocks that have lots of movement. I came up with the idea of using a basic linear regression model on the volume of stocks being traded by politicians, to predict how much they will be buying/selling in the following quarters. The graph will also show a trend of growing activity of trading from politicians, which can lead to more chances of insider trading. This would specifically fit the journalist persona, having a visual of simply more and more trading, with more profit is suspicious. I scraped capitol trades again, but rather than grabbing all the data, I wanted the volume from custom date ranges. I ran into issues when scraping and had to use bff instead of www, due to how the html was formatted, and loop through the pages and sum the volume. Then we added the regression. I moved onto the second model where I did some research and found the LSTM would be an ideal model for the data we had on stocks. I started with the LSTM model by looking at sample code, and trying to understand how it works with it being a subset of an RNN, I made an RNN first with the stock data into both python files. The actual LSTM is not finished and throws an error which I cannot figure out right now, but the two python files and the RNN run.  