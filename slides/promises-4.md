## Using Promises

Handling multiple asynchronous results in parallel:

```js
function asyncFunc() {
    return Promise.all([
        otherAsyncFunc1(),
        otherAsyncFunc2(),
    ]).then(([result1, result2]) => {
        console.log(result1, result2);
    });
}
```

<div class="fragment">
Handling errors:

<pre><code>
function asyncFunc() {
    return otherAsyncFunc1()
        .then(result1 => {
            console.log(result1);
            return otherAsyncFunc2();
        })
        .then(result2 => {
            console.log(result2);
        })
        .catch(err => {
            console.error(err);
        })
}
</code></pre>
</div>
