# ScPortM
An API to monitor & collect stock prices.

## Visit - (Link to be available soon)

## Documentation:

1. __/ (index url)__ : Provides json output for select stock prices
2. __/list__ : Provides dictionary of currently monitored stocks and their 'ids'
3. __/update__: Updates stock data to current value & price deviation (scheduled to run at an interval of 10 minutes by default)
4. __/background__: Updates parameters like market cap, high, low, np_qtr etc (scheduled to run at 12:30AM🕧 daily)
5. __/mk?q=""&tk=""__: Adds stock to be monitored. 'q' accepts tinker name of stock & 'tk' accepts company id as per screener's peer api (to be found in console)<br>
   Sample: using https:/`<domain>`/mk?q=RELIANCE&tk=2839201 adds Reliance to the list of companies to be monitored. (the tk value provided here is inaccurate)
6. __/rm?q=""__: Removes stock to be monitored. 'q' accepts the tinker name of stock. <br>
   Sample: using https:/`<domain>`/rm?q=RELIANCE removes Reliance from the list of companies to be monitored.

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
