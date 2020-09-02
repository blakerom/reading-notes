# TCP Servers

### Transmission Control Protocol
Is a standard that defines how to establish and maintain a network conversation through which applications can exchange data.

TCP works with IP in sending packets of data to and from your computer.
TCP is a connection oriented protocol, it establishes and maintains connection until the application at each end finishes exchanging messages.
This protocol is mainly used for organizing data in a way that ensures the secure transmission between the server and client. It establishes the rules and standard procedures for the way  information is communicated over the internet.

#### Example TCP server in ES6
##### Server
```js
'use strict';
 
// load the Node.js TCP library
const net = require('net');
const PORT = 1234;
const HOST = 'localhost';
 
class Server {
 constructor(port, address) {
  this.port = port || PORT;
  this.address = address || HOST;
  
  this.init();
 }
 
 init() {
  let server = this;
 
  let onClientConnected = (sock) => {
 
   let clientName = `${sock.remoteAddress}:${sock.remotePort}`;
   console.log(`new client connected: ${clientName}`);
 
   sock.on('data', (data) => {
    console.log(`${clientName} Says: ${data}`);
    sock.write(data);
    sock.write('exit');
   });
 
   sock.on('close', () => {
    console.log(`connection from ${clientName} closed`);
   });
 
   sock.on('error', (err) => {
    console.log(`Connection ${clientName} error: ${err.message}`);
   });
  }
 
  server.connection = net.createServer(onClientConnected);
 
  server.connection.listen(PORT, HOST, function() {
   console.log(`Server started at: ${HOST}:${PORT}`);
  });
 }
}
module.exports = Server;
```
##### Client
```js
'use strict';
 
const net = require('net');
const PORT = 1234;
const HOST = 'localhost';
 
class Client {
 constructor(port, address) {
  this.socket = new net.Socket();
  this.address = address || HOST;
  this.port = port || PORT;
  this.init();
 }
 init() {
  var client = this;
 
  client.socket.connect(client.port, client.address, () => {
   console.log(`Client connected to: ${client.address} :  ${client.port}`);
   client.socket.write('Hello World!');
  });
 
  client.socket.on('data', (data) => {
   console.log(`Client received: ${data}`);
   if (data.toString().endsWith('exit')) {
    client.socket.destroy();
   }
  });
 
  client.socket.on('close', () => {
   console.log('Client closed');
  });
 
  client.socket.on('error', (err) => {
   console.error(err);
  });
 
 }
}
module.exports = Client;
});
```

