Instructions for cointickerportfolio.py


What I am currently working on:
1. include: best performing coin (24hrs), total marketcap, profit of portfolio
2. error: when 404 on url, then the values are updated incorrectly (16.18 - 8.53)
3. Improve GUI
4. Plot some data?

# install for HyperPixel 4.0 (display)
Only follow these instructions. It will save you a lot of time:
https://learn.pimoroni.com/tutorial/sandyj/getting-started-with-hyperpixel-4

# install for Phat/What (display)
https://learn.pimoroni.com/tutorial/sandyj/getting-started-with-inky-phat


# to read-write the csv files install Pandas
sudo apt-get install python3-pandas

# Configticker.csv
Create a file called configticker.csv with the following content (just copy and paste):
summemax;0.1;2011-08-05 10:58
basemax;0.01;2011-08-05 10:58

summemax = the current value of your portfolio in USD
basemax = the current value of your portfolio in BTC
You need to do this only onece at the start. After that, the program will maintain these values

# Portfolio.csv
Create a file called portfolio.csv that includes your portfolio
Column coin: this will be used to complete the CoinGecko URL: https://api.coingecko.com/api/v3/coins/ampleforth
Column Qty: quantity in your portfolio

# to let the program automatically start after reboot
crontab -e

insert the following code at the end:
@reboot python3 /home/pi/CryptoTickerPortfolio.py &

# C Button on display
To stop the program, click on the "C" button. 
