---
layout: post
title: Stock Info Bot
subtitle: A reddit bot that displays the last closing price information of a stock on financial subreddits
bigimg: /img/black-and-white-chart-cost-241544.jpg
tags: [reddit-bot, bot, stock-info-bot]
---

Stock Info Bot is a reddit bot designed for financial subreddits that displays the last closing price and other related information of a stock on Reddit when invoked. 

The bot displays the last closing price, 1 wk high and lows, 1 mnth high and lows, 52 wk high and lows whenever it is triggered by the command as follows: $(stock ticker). For example, writing $AAPL in a reddit discussion thread will invoke the Stock Info Bot within seconds and the original poster will see the information below their comment.

The bot is hosted on Amazon AWS EC2 and utilizes two financial data sources, namely, Alpha Vantage and Barchart to maintain uptime and accuracy. 

On the technologies side of things, Stock Info Bot uses the official PRAW library to authenticate and login to Reddit as a bot. It is also used to fetch comment streams and reply to the comments accordingly. The Pandas data manipulation library is used to manipulate and gather data from the stock ticker CSV file. After Stock Info Bot replies to a person's comment, the data is stored in Amazon's NoSQL DynamoDB database. 

Finally, Stock Info Bot uses some in-built Python libraries such as requests (for HTTP requests), time / datetime / timedelta / pytz libraries to show accurate time and then the OS library to read and write files.

The bot is made by me, Sumit Agrawal. I am a Computer Science major studying at Suffolk University and I graduate in May 2020. I am currently looking for full-time job opportunities as a Software Engineer or other related job positions. Please contact me at sumit.r.agr [at] gmail.com for my resume and other information.

You can view the entire codebase for Stock Info Bot below.

Stock Info Bot's Code: [Github Link](https://github.com/SumitAgr/StockInfo-Bot)
