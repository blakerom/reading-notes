# Heroku Deployment

Heroku allows you to run a runtime server via Node.js that allows you to build server-side and networking applications.

1. This gives you your own client-server model.
2. Provides non-blocking and event-driven behavior.
3. Performs request for resource, receives data.
4. Use Heroku cloud application to turn into a World Wide Web

Basic server.js file to get started on your server includes

```js
var http = require("http");
var fs = require("fs");
var path = require("path");
var mime = require("mime");
```

To send a 404:

```js
function send404(response) {
  response.writeHead(404, {"Content-type" : "text/plain"});
  response.write("Error 404: resource not found");
  response.end();
}
```

You may then send a simple page in its place or redirect.

Create an HTTP server.

```js
var server = http.createServer(function(request, response) {
  var filePath = false;

  if (request.url == '/') {
    filePath = "public/index.html";
  } else {
    filePath = "public" + request.url;
  }

  var absPath = "./" + filePath;
  serverWorking(response, absPath);
});
```

Start your own server locally with `node server.js`.

