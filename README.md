# Genetic-Algorithm---Portfolio-Allocation

This repository contains a very simple genetic algorithm approach for creating a large-cap equity portfolio from Sensex BSE stocks

Stocks with significant market capitalization are chosen, each one from a different sector - HDFC Bank from banking, ITC from FMCG
(though involved in cigarettes business significantly!), Mahindra and Mahindra from auto, L&T from infrastructure, TCS from IT
services, and Sun Pharmaceuticals from pharmaceuticals

For each of these stocks, the closing price for each month, starting from June 2015 to June 2018 is obtained from www.moneycontrol.com (please find csv files along with the code)

3-month, 6-month, 12-month, 18-month, 24-month and 36-month returns are calculated and for each stock, the returns are aggregated
in a weighted manner, with a higher for for more recent 'n-month' returns

A simple genetic algorithm (with many assumptions and only one constraint!) is implemented to create a portfolio with the mentioned stocks. A few of the assumptions are: 
1. The mentioned stocks were a part of Nifty 50 throughout the given time-frame, and trading was not halted for these
2. The weightage of each stock in portfolio will only be in accordance with the returns. No other factors such as risk (or standard deviation), dividend payouts etc have been considered
3. Th weightage given to 'n-month' return is based on time series concept - the more recent price levels (or 'n-month' returns in this case) should be given higher weightage (we can probably make it better by using exponential smoothing instead of hard coding!)

Please ensure you have 'jupyter notebook', and other python libraries 'pandas' and 'numpy' installed on your systems. You can run jupyter notebook using anaconda environment (https://www.anaconda.com/download/). To install python libraries, use 'pip'. 

Note: The comments are included in code for understandability. This example does not, in any manner, recommends purchase of the mentioned, or any other stocks. This is just an example to demonstrate power and applications of genetic algorithms.  
