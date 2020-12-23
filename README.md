### Stocks least correlated with Covid-19 stock market decline?
The stock market took a hit during the ramp up of the Covid-19 pandemic.

My partner asked if any stocks were inversely correlated with the overall market decline. 

Using R + open-source data analysis packages we can quickly get at a first pass answer.

This post is not financial advice. 

Code for this post can be found on Github.

To represent the market we can pick an index to compare price trends against.

For this exploratory analysis, the S&P 500 index was selected. VFINX (Vanguard 500 Index Fund) is used as the proxy for the market and S&P 500.

First, we can take a look at what stocks make up the S&P 500.

Not surprisingly tech stocks have some of the highest weights in the index (as the S&P 500 is a market value weighted index). 

![SP 500 Stocks](https://github.com/bm-datalab/stocks_least_correlated_with_Covid-19_stock_market_decline/blob/master/Figs/sp500_stock_weights_top_50.jpeg?raw=true)

Without leaving R, we can pull in closing stock price data and plot stock price movements vs VFINX. 
We can see that many stocks were priced highest in February. News around Covid-19 sent the market tumbling down in March.

![SP 500 Stock Price Trends](https://github.com/bm-datalab/stocks_least_correlated_with_Covid-19_stock_market_decline/blob/master/Figs/sp500_least_correlated_stocks-1.jpeg?raw=true)

After comparing closing price correlations with VFINX, we can plot the 20 least correlated stocks. Stocks related to biotech, working from home tech, and consumer goods look to be least correlated with the S&P 500 market downturn.

![Stocks least correlated](https://github.com/bm-datalab/stocks_least_correlated_with_Covid-19_stock_market_decline/blob/master/Figs/sp500_least_correlated_stocks_grid.jpeg?raw=true)

Thank you to the R package developers that helped make this analysis seamless.
Tidyverse
Tidyquant
Scales
Ggrepel

p.s. my partner was pleased with the investigation findings. 
