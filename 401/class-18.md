# Sockets

A computer communications protocol providing full-duplex channels over a TCP connection.

### Setup
```js
const io = require('socket.io')();
// or
const Server = require('socket.io');
const io = new Server();
```
### New Server Options
```js
const io = require('socket.io')({
  path: '/test',
  serveClient: false,
});

// either
const server = require('http').createServer();

io.attach(server, {
  pingInterval: 10000,
  pingTimeout: 5000,
  cookie: false
});

server.listen(3000);

// or
io.attach(3000, {
  pingInterval: 10000,
  pingTimeout: 5000,
  cookie: false
});
```
### Server sockets
```js
io.sockets.emit('hi', 'everyone');
// is equivalent to
io.of('/').emit('hi', 'everyone');
```
### Server 'of'
```js
const adminNamespace = io.of('/admin');
```




