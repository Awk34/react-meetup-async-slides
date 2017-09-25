## Callbacks

```js
console.log('Ah CHOO!')

setTimeout(() => {
    console.log('gesundheit');
}, 2 * 1000);
```

```js
let httpRequest = new XMLHttpRequest();
httpRequest.onreadystatechange = alertContents;
httpRequest.open('GET', 'test.html');
httpRequest.send();

function alertContents() {
    if(httpRequest.readyState === XMLHttpRequest.DONE) {
        if(httpRequest.status === 200) {
            alert(httpRequest.responseText);
        } else {
            alert('There was a problem with the request.');
        }
    }
}
```
