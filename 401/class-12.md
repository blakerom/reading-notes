# OAuth

Authorization meant to authorize a service for another service.

![](https://a.slack-edge.com/fbd3c/img/api/articles/oauth_scopes_tutorial/slack_oauth_flow_diagram.png)

To begin: 
 - Register a new app with the service
 - Provide a redirect URI
 - Store the client ID and secret keys
 - Get Authorization from the user
 - Send authorization to the service and receive protected information
 
### Web Server Apps 
The most common types of applicaitons you will encounter when dealing with OAuth. They are written on server side where the source code is not publicly available.

### Single-Page Apps
Run entirely int he browser after loading the source code from a web page. Since ran in teh web page they are unable to maintain secrecy.


##### Resources
https://aaronparecki.com/oauth-2-simplified/
