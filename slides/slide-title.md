## The Stack (synchronous)

<div style="display: flex">
<div style="flex-grow: 1">
```js
function foo(b) {
  var a = 10;
  return a + b + 11;
}

function bar(x) {
  var y = 3;
  return foo(x * y);
}

console.log(bar(7));
```
</div>
<div style="flex-grow: 1">
<table>
    <thead>
        <tr>
            <th>function</th>
            <th>arguments</th>
            <th>returns</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>`foo`</td>
            <td>`b = 21`</td>
            <td>`a + b + 11`/`10 + 21 + 11`/`42`</td>
        </tr>
        <tr class="fragment" data-fragment-index="1">
            <td>`bar`</td>
            <td>`x = 7`</td>
            <td>return of `foo(x * y)`</td>
        </tr>
        <tr>
            <td>console.log</td>
            <td>return of <code>bar</code></td>
            <td></td>
        </tr>
    </tbody>
</table>
</div>
</div>


note:
    Put your speaker notes here.
    You can see them pressing 's'.

