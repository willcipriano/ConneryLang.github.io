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
Connery has native HTTP support via the http builtin. This can be used to make requests via http or https.
```
http URL 
``` 

| Variable            | Purpose                                                                                       |
|:--------------------|:----------------------------------------------------------------------------------------------|
| URL                 | A string containing the URL you wish to request                                               |
| HEADERS             | A list of any request headers you would like to use to make the request in "KEY:VALUE" format.|
| BODY                | A string used as a body for post requests. (not required for GET)                             |
 
http returns a dictionary containing many items that describe the request and provides the context.
```
connery> http "google.com"
response code : 301
headers : Dictionary
body : "<HTML><HEAD><meta http-equiv="content-type" ...
size : Dictionary
speed : Dictionary
time : Dictionary
url : "google.com"
```
As you can see size, speed and time are themselves dictionaries. They contain metrics about the request.
```
connery> grab (http_get "google.com") "time"
total : 0.103757
start : 0.103726
dns : 0.00437
connect : 0.018038
redirect : 0
ssl : 0
prestart : 0.018189
```