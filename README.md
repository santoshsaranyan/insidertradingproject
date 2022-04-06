# Insider Trading Analysis

Project on Analysis of Insider Trading Data using Form 4 Filings from the SEC Website (https://www.sec.gov/edgar/search-and-access)

• Web scraped insider filing and stock price data from Form 4 filings from the U.S Securities and Exchange
Commission (SEC) website and the Yahoo Finance API respectively, using Python.

• Analysed in R, the aspects of insider trading such as how the trading behaviour of insiders changed over time or
by their position, as well as whether there was a correlation between insider trading and stock prices of the
company.

• Discovered that purchases made by insiders have a positive correlation with the stock prices of their company

WebsScraping.ipynb contains code to get data from the Form 4 filings.
Project-Tidying.rmd focuses on analysing this data.

Some Visualizations I made during the analysis:
<img src="https://user-images.githubusercontent.com/63654605/162072327-34425959-2328-48df-9689-3ed2da342b5f.png" width="90%"></img> 

The above visualization shows if the price of a stock that was purchased by an insider a month before, increased or decreased in the years of 2019 and 2020. It is observed that the prices of stocks purchased by insiders usually increase a month after they purchase them. Only a few stocks that the insiders bought seem to decrease in price except during March-April 2020 (COVID-19), which confirms that a lot of stocks decreased in price during that period. 

<img src="https://user-images.githubusercontent.com/63654605/162072333-d677850f-6dca-46dc-8897-ff7a63fe0c21.png" width="90%"></img> 

This visualization shows if the price of a stock that was purchased by an insider six months before, increased or decreased in the years of 2019 and 2020. Unlike the previous graph, before March 2020, the number of shares that increase and decrease seems to go almost hand in hand. This could be due to the stock prices changing due to external factors and not because an insider bought them. After the COVID-19 period, many stocks increase compared to ones that decrease which are probably because a lot of insiders bought stocks when their prices were low during the dip, and these stocks increased in price after the market stabilized. 

<img src="https://user-images.githubusercontent.com/63654605/162072331-0d86eb80-fddd-4265-b57d-3b31ed00c158.png" width="90%"></img> 

This shows how the price of a stock that was sold by an insider a month before changed in price. Much, like the graph for the six-month purchases, there is not a clear distinction between the number of stocks that increase or decrease. This is mostly because the employees are paid in or acquire a lot of their company’s stocks and they simply sell for their expenditure and not because they know their company’s value is going to go down.

<img src="https://user-images.githubusercontent.com/63654605/162072332-ae2dc701-62e1-4c5c-a32a-77ed99d242c8.png" width="90%"></img> 

The percent of shares that increase in price is plotted against the number of shares that were involved in a transaction. As we limit the number of transactions to include only those with a certain high amount of shares per transaction, it is found that the percentage of shares that increase greatly goes up. There is a jump from 62% to 68% at 10,000 shares and more and it even goes above 70% at 20,000 shares and more. We take the optimal value of 10,000 shares for a balance between a high increase in the percent of shares that go up and the number of observations for those values. 
