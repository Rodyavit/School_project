# Portfolio data processing
-The goal of this data processing was to update a power BI dashboard on a daily basis
-Therefore, the notebook of this folder was run on databricks and scheduled to run once a day 
-The code took as input an xlsx file with portfolio data info from a container in a azure storage account then thanks to python and yfinance library we obtain a list of the company from the portfolio which are still listed on stock exchange and those which are no longer. Afterwards, it obtains the historical value of the sticker from 2016 until the day before.
-On the other hand thanks to finhub API we obtain external info concerning the tickers like the type of industry, advice on whether to buy or sell tickers etc...
-After all the processing, the results were uploaded as a csv format into the same container as the input in order to enable the Power Bi dashboard to be updated daily.