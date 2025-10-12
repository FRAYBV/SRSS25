## Descripción
Help us test the form by submiting the username as `test` and password as `test!`
Additional details will be available after launching your challenge instance.
## Solución
```
curl -v -d 'username=test&password=test!' http://sat
urn.picoctf.net:50536/login
*   Trying 13.59.203.175:50536...
* Connected to saturn.picoctf.net (13.59.203.175) port 50536 (#0)
> POST /login HTTP/1.1
> Host: saturn.picoctf.net:50536
> User-Agent: curl/7.81.0
> Accept: */*
> Content-Length: 28
> Content-Type: application/x-www-form-urlencoded
> 
* Mark bundle as not supporting multiuse
< HTTP/1.1 302 Found
< X-Powered-By: Express
< Location: /next-page/id=cGljb0NURntwcm94aWVzX2Fs
< Vary: Accept
< Content-Type: text/plain; charset=utf-8
< Content-Length: 60
< Date: Sat, 11 Oct 2025 18:14:42 GMT
< Connection: keep-alive
< Keep-Alive: timeout=5
< 
* Connection #0 to host saturn.picoctf.net left intact
FRAY30-picoctf@webshell:~$ curl -L -v -d 'username=test&password=test!' http://
saturn.picoctf.net:50536/login
*   Trying 13.59.203.175:50536...
* Connected to saturn.picoctf.net (13.59.203.175) port 50536 (#0)
> POST /login HTTP/1.1
> Host: saturn.picoctf.net:50536
> User-Agent: curl/7.81.0
> Accept: */*
> Content-Length: 28
> Content-Type: application/x-www-form-urlencoded
> 
* Mark bundle as not supporting multiuse
< HTTP/1.1 302 Found
< X-Powered-By: Express
< Location: /next-page/id=cGljb0NURntwcm94aWVzX2Fs
< Vary: Accept
< Content-Type: text/plain; charset=utf-8
< Content-Length: 60
< Date: Sat, 11 Oct 2025 18:16:11 GMT
< Connection: keep-alive
< Keep-Alive: timeout=5
< 
* Ignoring the response-body
* Connection #0 to host saturn.picoctf.net left intact
* Issue another request to this URL: 'http://saturn.picoctf.net:50536/next-page/id=cGljb0NURntwcm94aWVzX2Fs'
* Switch from POST to GET
* Found bundle for host saturn.picoctf.net: 0x5556463b8020 [serially]
* Can not multiplex, even if we wanted to!
* Re-using existing connection! (#0) with host saturn.picoctf.net
* Connected to saturn.picoctf.net (13.59.203.175) port 50536 (#0)
> GET /next-page/id=cGljb0NURntwcm94aWVzX2Fs HTTP/1.1
> Host: saturn.picoctf.net:50536
> User-Agent: curl/7.81.0
> Accept: */*
> 
* Mark bundle as not supporting multiuse
< HTTP/1.1 200 OK
< X-Powered-By: Express
< Content-Type: text/html; charset=utf-8
< Content-Length: 264
< ETag: W/"108-PlcOMYcBpM14tkoLrMSzu1ev8gg"
< Date: Sat, 11 Oct 2025 18:16:11 GMT
< Connection: keep-alive
< Keep-Alive: timeout=5
< 
<!DOCTYPE html>
<head>
    <title>flag</title>
</head>
<body>
    <script>
        setTimeout(function () {
           // after 2 seconds
           window.location = "/next-page/id=bF90aGVfd2F5X2RmNDRjOTRjfQ==";
        }, 0.5)
      </script>
    <p></p>
* Connection #0 to host saturn.picoctf.net left intact
</body>FRAY30-picoctf@webshell:~$ echo 'cGljb0NURntwcm94aWVzX2FsbF90aGVfd2F5X2RRjfQ==' | base64 -d
picoCTF{proxies_all_the_way_df44c94c}
```
## Notas adicionales

## Referencias