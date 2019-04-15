
## HTTP Requests
Within an application, what are we trying to do?

* Send a message
* Get a response

Notes:

* HyperText Transport Protocol
* Just programmatically making requests in this talk

---

## HTTP Message to send

<img src="slides/images/request.svg" style="background: white" />

```http
GET / HTTP/1.1
Host: phpne.org.uk
Accept: image/gif, image/jpeg, */*
Accept-Language: en-us
```

Notes:

* The request is just text
* Has a header and an optional payload (body)
* Rules on how it is constructed

---

## HTTP Message response

<img src="slides/images/response.svg" style="background: white" />

```http
HTTP/2.0 304 Not Modified
date: Sat, 13 Apr 2019 19:14:59 GMT
via: 1.1 varnish
cache-control: max-age=600
etag: W/"5c80f5e9-2626"
expires: Sat, 13 Apr 2019 19:24:42 GMT
age: 16
```

Notes:

* Response is text similar to the request
