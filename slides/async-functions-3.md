## async functions

<pre><code style="max-height: 100%">
async function buyStockOneDollarLower(name) {
    try {
        let symbol = await getStockSymbol(name);

        let currentStockPrice = await getCurrentStockPrice(symbol);

        await buyStock(symbol, currentStockPrice - 1);

        console.log('Purchase order placed');
    } catch(err) {
        console.error(err);
    }
}

buyStockOneDollarLower('Microsoft');
</code></pre>

Note:
    Still get unified catching, but with familiar try/catch
    replace `.then(cb)` with just `= await`
    looks like sync code, but doesn't block
