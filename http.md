# HTTP
Connery has native HTTP support via the http builtin. This can be used to make get and post requests via http or https.
```
;get request
http GET URL HEADERS

;post request
http POST URL HEADERS BODY
``` 

_URL_: The url you would like to make a request to.

_HEADERS_: A list of any request headers you would like to use to make the request in "KEY:VALUE" format.

_BODY_: A string used as a body for post requests.
 
http returns a list with three items.
```
{STATUS_CODE {HEADERS} RESPONSE_BODY}
```
_STATUS_CODE_: A number representing the status code 

_HEADERS_: A list containing each header sent by the server. In "Key: Value" format.

_RESPONSE_BODY_: A string that contains the body of the response.

### http request examples

An example get request to google.com with the foo header set to bar.
```
http GET "google.com" (list "foo:bar")
```

An example post to google.com with no headers.
```
http POST "google.com" None "this is the post body"
```

### Helper functions
The http_get helper function only requires a url to make a request.
```
http_get "connerylang.org"
```

The http_post helper function takes a url and a post body.
```
http_post "connerylang.org" "Bond, James Bond."
```

The http_status_code_text function takes a response and returns a textual representation of the status code.
```
http_status_code_text (http_get "connerylang.org")
```
```
"OK"
```
