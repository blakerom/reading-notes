# EJS

Set-up server file for use of Express JS.

```js
var express = require('express');
var bodyParser = require('body-parser');
var cors = require('cors');
var path = require('path');

var app = express();

app.use(bodyParser());
app.use(cors());

app.set('views, path.join(_dirname, 'views'));
app.set('view engine', 'ejs');
```

Path is a built in core module for Node. It takes in two paths and joins them on any views engine we concatenate the current working directory in a folder named views.
