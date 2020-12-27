---
title: Stock Prices API
week: 11
homework: 1
---

Many software companies and some hobbyists provide web APIs (application programming interface) that allow us
to interact with their software by making network requests.  For this assignment, we will be using the FinHub
API which is available for free subject to certain usage limits.  With the free tier we'll be using, you will
only be able up to 30 API requests per second.  Sign-up to receive a free API from https://finhub.io 

**IMPORTANT**: When you sign up for an account you will get what's called an API key to make your requests. You
should _NOT_ add this key to your GitHub submission.  See the comments for the sample code for more information
on how to protect this key.

Your goal is to write a project to retrieve stock quotes.  The user will be presented with a command prompt where they
can input a stock symbol.  The program should then make a request to the Finhub API and present the user with the latest
information for that stock.

The API request you are going to use is `https://finnhub.io/api/v1/quote?symbol=<symbol>&token=<api_key>`

It will give you five attributes back.  They use very short names to identify everything to save on network traffic.
When you display the information to your user, you should use longer, more descriptive labels:

* o - Open price of the day
* h - High price of the day
* l - Low price of the day
* c - Current price
* pc - Previous close price
