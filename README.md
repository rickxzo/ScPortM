# ScPortM
## An API to monitor & collect stock prices.

## Visit - (Link to be available soon)

## Documentation:

1. / (index url) : Provides json output for select stock prices. <br>
2. /list : Provides dictionary of currently monitored stocks and their 'ids'. <br>
3. /update: Updates stock data to current value (scheduled to run at an interval of 10 minutes by default)
4. /mk?q=""&tk="": Adds stock to be monitored. 'q' accepts tinker name of stock & 'tk' accepts company id as per screener's peer api (to be found in console)
   Sample: using https:/<domain>/mk?q=RELIANCE&tk=2839201 adds Reliance to the list of companies to be monitored. (the tk value provided here is inaccurate)
6. /rm?q="": Removes stock to be monitored. 'q' accepts the tinker name of stock.
   Sample: using https:/<domain>/rm?q=RELIANCE removes Reliance from the list of companies to be monitored.


