# webpack-dev-server-global

This repo shows how webpack-dev-server fails if `node.global = false` is set
on the webpack configuration.


## Running the repro

- `npm install`
- `npm run serve`


```
Uncaught ReferenceError: global is not defined
    at Object.<anonymous> (browser-crypto.js:3)
    at __webpack_require__ (bootstrap 46c9e79f3cb14d538cb2:19)
    at Object.<anonymous> (random.js:4)
    at __webpack_require__ (bootstrap 46c9e79f3cb14d538cb2:19)
    at Object.<anonymous> (event.js:3)
    at __webpack_require__ (bootstrap 46c9e79f3cb14d538cb2:19)
    at Object.<anonymous> (websocket.js:3)
    at Object.<anonymous> (websocket.js:99)
    at __webpack_require__ (bootstrap 46c9e79f3cb14d538cb2:19)
    at Object.<anonymous> (transport-list.js:5)
```