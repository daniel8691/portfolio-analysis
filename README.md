# portfolio-analysis

## Introduction
For this project, I will use series of calculations and models that consider both risk and returns of the securities within my portfolio. These calculations will allow me to make well-informed decisions that is backed by data and hopefully maximize my investment returns. I will be using data from yahoo finance using panda's datareader and extract the adjusted closing prices for a more accurate reflection of stocks' value at market close.

Key numbers to look for in this analysis are the changes in percentage growth for the past 7 years, Diversifiable and non-diversifiable 
risks of the portfolio, the efficient frontier, Beta coefficient, CAPM and the Sharpe Ratio. I wanted to use a 10 year data but ended up using 7
because one of the securities in the portfolio only became publicly traded in 2013. 

## Data Source
I used the **Pandas Datareader** package that allowed me to create dataframes from various internet datasources. The source I chose for this analysis was Yahoo Finance, looking only at the adjusted closing prices

## Methodology

I will mostly focus on using the securities' variance and mean for the analysis. Dividends are also not accounted for in the analysis. 

When I calculate the annualized returns, I used 250 days because I am not including the days when the markets are closed

The defined risk for this analysis is the standard deviation of the stock which will be used to describe the volatility of the security
Securities that have high volatilities are deemed higher risk

## Analysis

![growth_comparison scaled](https://github.com/daniel8691/portfolio-analysis/blob/master/growth_comparison.jpg)

The graph describes the growth of each compay's stock prices starting from July 1, 2013. To make an accurate comparison, I normalized the data by dividing all prices for each stock by the first day of the analysis so that all stock prices start from 100. 

We can see that RY.TO (RBC) had the highest growth since 2013, followed by BCE.TO (Bell Canada), and SU.TO (Suncor) and BPY_UN.TO (Brookfield Property Partners) actaully achieved a negative growth since 2013. 

After constructing the efficient frontier, I found that the plot is negatively correlated, meaning that for this set of portfolio, the more risk I 
take, the less return I will receive. This may be possible because RBC and BCE are calculated to have low risk while producing high returns while 
the rest of the securities within the portfolio don't really produce high returns but bear higher risks than RBC and BCE

Looking at the plot, it can be said that if the structure of the portfolio is more weighted towards RBC and BCE, I will receive a higher return
on my investment, hence the negative correlation.

A major factor not included in this analysis is the dividend payouts. BPY enjoys a more luxurious dividend payout than the rest of the securities 
in the portfolio so even though my normalized plot displays BPY, along with SU, as low-return securities, their poor performance can be justified. 

When Calculating the Beta of the stock, I took the past 5 years of data because the companies' capital expenditures and business model are more recent.

Looking at the Sharpe Ratio, I can see that RY has the highest Sharpe ratio among other securities in the portfolio. I used the Sharpe Ratio 
to find out the risk-adjusted performance of the individual securities. With the standard deviation as the denominator, the higher 
a security's standard deviation (volatility) the lower the Sharpe Ratio will be.
