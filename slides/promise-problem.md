## The Problem with Promises

<pre><code style="max-height: 100%">
function getStockSymbol(name) {
  return http.get(`api/symbol/${name}`);
}
function getCurrentStockPrice(symbol) {
  return http.get(`api/price/${symbol}`);
}
function buyStock(symbol, price) {
  return http.post('api/buy', { symbol, price });
}

function buyStockOneDollarLower(name) {
    let symbol;

    return getStockSymbol(name).then(_symbol => {
      symbol = _symbol;
      return getCurrentStockPrice(_symbol);
    }).then(price => {
      price = price - 1;
      return buyStock(symbol, price);
    }).then(() => {
      console.log('Purchase order placed');
    }).catch(err => {
      console.error(err);
    });
}

buyStockOneDollarLower('Microsoft');
</code></pre>

Note:
    better than callbacks
    passing data between promise handlers
    clutter
