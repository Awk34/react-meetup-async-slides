## Understanding Promises

### A Promise is an event emitter

One way to view a Promise is as an object that emits events.

```js
function asyncFunc() {
    const eventEmitter = { success: [] };
    setTimeout(() => { // (A)
        for (const handler of eventEmitter.success) {
            handler('DONE');
        }
    }, 100);
    return eventEmitter;
}

asyncFunc()
    .success.push(x => console.log(`Result: ${x}`)); // (B)
```

Registering the event listener (line (B)) can be done after calling asyncFunc(), because the callback handed to setTimeout()
(line (A)) is executed asynchronously, after this piece of code is finished.

Normal event emitters specialize in delivering multiple events, starting as soon as you register.

In contrast, Promises specialize in delivering exactly one value and come with built-in protection against registering too late: the
result of a Promise is cached and passed to event listeners that are registered after the Promise was settled.
