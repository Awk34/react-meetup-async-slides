##  event-loop

![stack queue heap image](https://developer.mozilla.org/files/4617/default.svg)
![queue gif](https://media.giphy.com/media/b3RlcmZXKQ932/giphy.gif)

```js
while(queue.waitForMessage()) {
  queue.processNextMessage();
}
```
`queue.waitForMessage` waits synchronously for a message to arrive if there is none currently.

 - "Run-to-completion": Each message is processed completely before any other message is processed.
 - Adding messages: In web browsers, messages are added anytime an event occurs and there is an event listener attached to it.
 - Zero delays: Calling `setTimeout` with a delay of 0 immediately adds the callback to the event queue.
 - **Never blocking**: A very interesting property of the event loop model is that JavaScript, unlike a lot of other languages, never blocks.
