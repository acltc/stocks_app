# Stock Watcher

This project will be an app that allows a user to see the price history for the stocks of a publicly traded company. The user does this in two steps: 

1. First, the user enters into a form the company they're searching for. This may be the entire company name or even just part of the company name. For example, the user may search for "Microsoft" or even just "Micr". The app will then return all a list of stock symbols that match the company that the user was searching for. If the user searched for "Microsoft", this will return one stock symbol as a search result: "MSFT".
2. Then, the user can click on one of the search results (e.g. "MSFT"), and a graph showing the prices of the stock for the past 30 days will appear.

## Search API

For the first part of this app, you'll be making your own API that allows a user to search for stock symbols by supplying a search query. That is, the API will accept a search query like "micr" and return all stock symbols corresponding to companies that have "micr" somewhere in their full names.

To obtain this data, you can download the CSV found here: https://www.nasdaq.com/market-activity/stocks/screener. (There's a button there that says "Download CSV"). Included in this CSV are all publicly traded companies and their respective stock symbols. 

You'll have to write a script that takes this data and puts it in a database. Your API can then return the data from this database. It's up to you as to how the API works exactly (such as the exact API endpoints and how the returned JSON is formatted). The main thing is that the API will accept a search parameter representing a company name (or part of a company name) and return all stock sybmols that match the search.

## Stock Price Chart

To get the stock price data, you'll use the [third-party API provided by IEX Cloud](https://iexcloud.io/docs/api/). You'll have to sign up for an API key, but there's a free plan that allows you a limited number of API calls.

When the user clicks on a stock symbol, a chart will be rendered showing the prices of that stock for the last 30 days. You can use the "close" value of the stock for each day.

## Bonus

Instead of just displaying a simple graph, use a candlestick chart to display data of the the stock's low, high, open, and close prices. See an example here: https://apexcharts.com/javascript-chart-demos/candlestick-charts/basic/


