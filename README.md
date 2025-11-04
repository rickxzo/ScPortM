# ScPortM
An API to monitor & collect stock prices.

## Visit - https://scportm-code.onrender.com

## Documentation:

1. __/ (index url)__ : Provides json output for select stock prices
2. __/list__ : Provides dictionary of currently monitored stocks and their 'ids'
3. __/update__: Updates stock data to current value & price deviation (scheduled to run at an interval of 10 minutes by default)
4. __/background__: Updates parameters like market cap, high, low, np_qtr etc (scheduled to run at 12:30AM🕧 daily)
5. __/mk?q=""&tk=""__: Adds stock to be monitored. 'q' accepts tinker name of stock & 'tk' accepts company id as per screener's peer api. (to be found in console)<br>
   Sample: using https://`<domain>`/mk?q=RELIANCE&tk=2839201 adds Reliance to the list of companies to be monitored. (the tk value provided here is inaccurate)
6. __/rm?q=""__: Removes stock to be monitored. 'q' accepts the tinker name of stock <br>
   Sample: using https://`<domain>`/rm?q=RELIANCE removes Reliance from the list of companies to be monitored.
7. __/ck?q=""__: Changes the price change %age alert coefficient (custom feature). Note: use q=NC to get the current value.
8. __/buy?q=""__: Marks buying of a stock at current price. 'q' accepts tinker name of stock.
9. __/sell?q=""__: Erases buying of the last bought lot of a stock. 'q' accepts tinker name of stock.
10. __/portfolio__: View the currently held stocks and their price at time of buying.

Note: Finding tk param for /mk is a complicated process. For testing purposes, here's a sample stock {'CPPLUS': 141593375}. <br>
Otherwise, just note the tinker and id for a pre-existing stock, /rm it and then proceed to use the tinker and id to /mk it. <br>
Mail to rickxzo.perz@gmail.com for any form of inquiry.


### __/ (index url)__ return format:
#### JSON Structure
```json
[
   {
      "book": "",
      "deviation": "",
      "high": "",
      "low": "",
      "market_cap": "",
      "name": "",
      "np_qtr": "",
      "pe": "",
      "price": "",
      "qtr_profit_var": "",
      "qtr_sales_var": "",
      "roce": "",
      "roe": "",
      "sales_qtr": "",
      "tag": ""
   }
]
```

### Additional Features (Client):

1. Mail buy/sell alerts to client based on custom rules.
2. Display 'tag' param to highlight stock movement based on custom rules.
