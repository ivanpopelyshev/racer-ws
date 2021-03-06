# racer-ws

[![NPM](https://nodei.co/npm/racer-ws.png?downloads=true)](https://nodei.co/npm/racer-ws/)

This is a plugin to use racer over a websocket connection. If you also need fallback to browserchannel use [racer-highway](https://github.com/derbyparty/racer-highway).

## Usage

In the server part of your app:

```js
var racerWS = require('racer-ws'); 

// ...
// var server = http.createServer
// ...

// ...
// var store  = racer.createStore 
// or
// var store  = derby.createStore
// ...

var upgrade = racerWS(store);

// ...

server.on('upgrade', upgrade)
```

If you use `racer-ws` with derby make sure `racerWS(store)` is before any calls to `app.writeScripts`.

## WebSocket Info

* [What is WebSocket?](https://www.websocket.org/)
* [Nginx WebSocket Info](http://nginx.org/en/docs/http/websocket.html)
* [Heroku WebSocket Info](https://devcenter.heroku.com/articles/websockets)

## MIT License
Copyright (c) 2014 by Artur Zayats

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
