## Understanding Promises

```js
function asyncFunc() {
    return new Promise((resolve, reject) => {
        setTimeout(() => resolve('DONE'), 100);
    });
}

asyncFunc()
    .then(x => console.log(`Result: ${x}`));

// Output:
// Result: DONE
```

- Conceptually, invoking asyncFunc() is a blocking function call.
- A Promise is both a container for a value and an event emitter.
- More structured callbacks
- Three states:
  - pending: initial state, neither fulfilled nor rejected.
  - fulfilled: meaning that the operation completed successfully.
  - rejected: meaning that the operation failed.
