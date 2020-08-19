# Express Routing

### Response and Request
An event driven system that checks the route passed in and executes the response, request function in return.
'app.get('/thing', (req,res) => {})'

The *Request* object takes in parameters and Query strings.
'app.get('/api/:thing',...) = req.params.thing'
'http://server/route?ball=round = req.query.ball'

The *Response* object sendsback data to the browser.
This method also sends headers with cookies and status codes.

### Middleware
A series of functions that the requests go through. Each of these functions has a response, request, and a *Next* as parameters.
There are two types of middleware, application and route.

Application
- Error handling
- Bringing in other routes
- Defaults
- JSON
- Runs on every request

Route
- specific
- logged in events
- ip address
- cookies

This is usefull for:
- Logging
- Dynamic Model laoding
- Browser, location, user info
- Consistent data

### Testing
Supertesting without turning the server on to run full tests on API calls.
Mock test to avoid ruining data and use fake data.
Test integrations connecting to other services.

