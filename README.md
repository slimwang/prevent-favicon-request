# prevent-favicon-request
A piece of code that can prevent the favicon request.

Sometimes you will run into the issue like this:
```
http://localhost:8080/favicon.ico
```
and then:
```
404 Not Found
```
to fix it, add this line of code in your html `head`
```
<link rel="icon" href="data:,">
```
Here is the explanation:

>The issue is, when the browser cache is empty and a user comes in, here is what happens:

>the user requests URL "/". This URL is cached. 

>the browser makes a requests to "/favicon.ico". This URL becomes the new URL where to redirect to upon authentication.

>the user posts the login form and is redirected to "/favicon.ico". 
