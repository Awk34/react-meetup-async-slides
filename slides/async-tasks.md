## Async tasks

 - Example Macro Tasks
   - `setTimeout` / `setInternal`
   - `setImmediate`
   - I/O tasks (Node.js `fs`, `XMLHttpRequest`)
 - Example Micro Tasks
   - process.nextTick
   - (native) Promises

![cookie monster waiting](https://media.giphy.com/media/o5oLImoQgGsKY/giphy.gif)

> Read more:
> - https://abc.danch.me/microtasks-macrotasks-more-on-the-event-loop-881557d7af6f
> - https://jakearchibald.com/2015/tasks-microtasks-queues-and-schedules/

note:
    For every tick of the event loop, one macrotask can be completed,
    but the whole microtask queue is processed
