# Lumen-CORS
CORS structure I have used in my Laravel / Lumen project

## Whats is CORS
Cross-Origin Resource Sharing (CORS) is an HTTP-header based mechanism that allows a server to indicate any other origins (domain, scheme, or port) than its own from which a browser should permit loading of resources. CORS also relies on a mechanism by which browsers make a “preflight” request to the server hosting the cross-origin resource, in order to check that the server will permit the actual request. In that preflight, the browser sends headers that indicate the HTTP method and headers that will be used in the actual request.

An example of a cross-origin request: the front-end JavaScript code served from https://domain-a.com uses XMLHttpRequest to make a request for https://domain-b.com/data.json.

For security reasons, browsers restrict cross-origin HTTP requests initiated from scripts. For example, XMLHttpRequest and the Fetch API follow the same-origin policy. This means that a web application using those APIs can only request resources from the same origin the application was loaded from unless the response from other origins includes the right CORS headers.  More->https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS

##How can I resolve the CORS error in the lumen?

#Step 1:
Create a file named CorsMiddleware.php in the app-> Http-> Middleware directory in the lumen project.

#Step 2:
Add the following code to the app.php file in the bootstrap folder in the home directory.
Root Folder -> bootstrap->app.php

<p float="left">
<img src="https://user-images.githubusercontent.com/6796645/107275361-b0c56d80-6a62-11eb-9d74-cadb2e220249.png">
</p>

#Done. Now our http requests will be passed through the cors middleware and the rules will be applied.

#Note 1:

