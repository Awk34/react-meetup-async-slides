## async functions

Handling multiple asynchronous results in parallel:

```js
async function asyncFunc() {
    const [result1, result2] = await Promise.all([
        otherAsyncFunc1(),
        otherAsyncFunc2(),
    ]);
    console.log(result1, result2);
}
```

<div class="fragment">
Handling errors:

<pre><code>
async function asyncFunc() {
    try {
        await otherAsyncFunc();
    } catch (err) {
        console.error(err);
    }
}
</code></pre>
</div>
