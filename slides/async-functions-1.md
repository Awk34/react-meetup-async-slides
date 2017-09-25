## async functions

Async functions always return a promise.
They wait on an `await` before continuing execution.

Handling a single asynchronous result:

```js
async function asyncFunc() {
    const result = await otherAsyncFunc();
    console.log(result);
}
```

<div class="fragment">
Handling multiple asynchronous results sequentially:

<pre><code>
async function asyncFunc() {
    const result1 = await otherAsyncFunc1();
    console.log(result1);
    const result2 = await otherAsyncFunc2();
    console.log(result2);
}
</code></pre>
</div>
