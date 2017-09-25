##  event-loop

```js
while(queue.waitForMessage()) {
  queue.processNextMessage();
}
```

`queue.waitForMessage` waits synchronously for a message to arrive if there is none currently.
