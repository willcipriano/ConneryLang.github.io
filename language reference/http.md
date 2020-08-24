---
layout: default
title: HTTP
parent: Language Reference 
nav_order: 7
---

# HTTP/HTTPS

### http
Builtin 
{: .label .label-purple }
Connery has native HTTP support via the http builtin. This can be used to make get and post requests via http or https.
```
;get request
http GET URL HEADERS

;post request
http POST URL HEADERS BODY
``` 

| Variable            | Purpose                                                                                       |
|:--------------------|:----------------------------------------------------------------------------------------------|
| URL                 | A string containing the URL you wish to request                                               |
| HEADERS             | A list of any request headers you would like to use to make the request in "KEY:VALUE" format.|
| BODY                | A string used as a body for post requests. (not required for GET)                             |
 
http returns a list with three items.

```
{STATUS_CODE {HEADERS} RESPONSE_BODY}
```

| Variable                   | Purpose                                                                      |
|:---------------------------|:-----------------------------------------------------------------------------|
| STATUS_CODE                | A number representing the status code                                        |
| HEADERS                    | A list containing each header sent by the server. In "KEY: VALUE" format.    |
| RESPONSE_BODY              | A string that contains the body of the response.                             |

### http request examples

An example get request to google.com with the foo header set to bar.
```
http GET "google.com" (list "foo:bar")
```

An example post to google.com with no headers.
```
http POST "google.com" None "this is the post body"
```

## Helper functions

### http_get
StdLib
{: .label .label-green }
The http_get helper function only requires a url to make a request.
```
http_get "connerylang.org"
```
### http_post
StdLib
{: .label .label-green }
The http_post helper function takes a url and a post body.
```
http_post "connerylang.org" "Bond, James Bond."
```

### http_status_code_text
StdLib
{: .label .label-green }
The http_status_code_text function takes a response and returns a textual representation of the status code.
```
http_status_code_text (http_get "connerylang.org")
```
```
"OK"
```