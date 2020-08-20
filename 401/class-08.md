# Express Routing and Connected API

Routing refers to the applications endpoints and how they respond to client requests. Using Express to define routing using methods withint he app that correspond to the HTTP methods. 
Some of the more common methods we will use are:
- app.get()
- app.post()
- app.put()
- app.delete()
- app.patch()

> app.param([name], callback)

Very basic route looks like:
```js
var express = require('express')
var app = express()

// respond with "hello world" when a GET request is made to the homepage
app.get('/', function (req, res) {
  res.send('hello world')
})
```

Routes that behave like middleware:
```js
app.get('/example/b', function (req, res, next) {
  console.log('the response will be sent by the next function ...')
  next()
}, function (req, res) {
  res.send('Hello from B!')
})
```

An Express router will require express and instantiate a variable to utilize its methods.
```js
const express = require('express');
const app = express();
```



