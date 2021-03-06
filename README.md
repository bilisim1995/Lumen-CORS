# Lumen-CORS
CORS structure I have used in my Laravel / Lumen project
<br>
### Version :monocle_face:
php artisan --version
```
Laravel Framework Lumen (8.2.1) (Laravel Components ^8.0)
```
<br><br><hr>

## What is CORS
Cross-Origin Resource Sharing (CORS) is an HTTP-header based mechanism that allows a server to indicate any other origins (domain, scheme, or port) than its own from which a browser should permit loading of resources. CORS also relies on a mechanism by which browsers make a “preflight” request to the server hosting the cross-origin resource, in order to check that the server will permit the actual request. In that preflight, the browser sends headers that indicate the HTTP method and headers that will be used in the actual request.

An example of a cross-origin request: the front-end JavaScript code served from https://domain-a.com uses XMLHttpRequest to make a request for https://domain-b.com/data.json.

For security reasons, browsers restrict cross-origin HTTP requests initiated from scripts. For example, XMLHttpRequest and the Fetch API follow the same-origin policy. This means that a web application using those APIs can only request resources from the same origin the application was loaded from unless the response from other origins includes the right CORS headers.  More->https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS
<br><br><br>
<hr>

## How can I resolve the CORS error in the lumen :question:

# Step 1:
Create a new file <ins>CorsMiddleware.php</ins> inside directory <ins>app\Http\Middleware</ins>

# Step 2:
Add the following code to the app.php file in the bootstrap folder in the root directory.
<ins> Root Folder->bootstrap->app.php </ins>
```
$app->middleware([
    App\Http\Middleware\CorsMiddleware::class
]);
```

### :partying_face: :ok_hand: Done. Now our http requests will be passed through the cors middleware and the rules will be applied. 
<hr>
<br><br><br>

### :grey_exclamation: Note: If you encounter an error like the following;
<br>
<p float="left">
<img src="https://user-images.githubusercontent.com/6796645/107275912-64c6f880-6a63-11eb-9588-0e912f6e7b93.PNG">
</p>
<br><br>

Root Folder -> bootstrap-> remove 3 written header codes in app.php file (remove 9,10,11 line)
<ins>bootstram->app.php</ins>
<p float="left">
<img src="https://user-images.githubusercontent.com/6796645/107276234-c5563580-6a63-11eb-8cba-bc1d5a429f54.jpg" width="400" height="254">
</p>
<br>
