# Stock-Reading
Enter stock ticker to get basic finances 
import pandas as pd
import yfinance as yf
import datetime
from datetime import date


import numpy as np

import matplotlib.pyplot as plt

from pandas.plotting import scatter_matrix
from pandas_datareader import data

start_date = '1990-01-01'
end_date = date.today()

ticker = input("stock: ")
stock = yf.download(ticker,start_date,end_date)

stock.tail(5)

stock['Open'].plot(label = 'Stock', figsize = (15,7))

start_date = '1990-01-01'
end_date = date.today()

ticker2 = input("stock: ")
stock2 = yf.download(ticker2,start_date,end_date)

stock2.tail(5)

stock2['Open'].plot(label = 'Stock2', figsize = (15,7))

