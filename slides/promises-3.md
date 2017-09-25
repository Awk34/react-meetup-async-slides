## Using Promises

Handling a single asynchronous result:

```js
function asyncFunc() {
    return otherAsyncFunc()
    .then(result => {
        console.log(result);
    });
}
```

<div class="fragment">
Handling multiple asynchronous results sequentially:

<pre><code>
function asyncFunc() {
    return otherAsyncFunc1()
        .then(result1 => {
            console.log(result1);
            return otherAsyncFunc2();
        })
        .then(result2 => {
            console.log(result2);
        });
}
</code></pre>
</div>
