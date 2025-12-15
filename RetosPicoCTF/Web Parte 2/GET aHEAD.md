## Descripción
Find the flag being held on this server to get ahead of the competition [http://mercury.picoctf.net:45028/](http://mercury.picoctf.net:45028/)
## Solución
```
curl -vv -I http://mercury.picoctf.net:45028/index.php
*   Trying 18.189.209.142:45028...
* Connected to mercury.picoctf.net (18.189.209.142) port 45028 (#0)
> HEAD /index.php HTTP/1.1
> Host: mercury.picoctf.net:45028
> User-Agent: curl/7.81.0
> Accept: */*
> 
* Mark bundle as not supporting multiuse
< HTTP/1.1 200 OK
HTTP/1.1 200 OK
< flag: picoCTF{r3j3ct_th3_du4l1ty_775f2530}
flag: picoCTF{r3j3ct_th3_du4l1ty_775f2530}
< Content-type: text/html; charset=UTF-8
Content-type: text/html; charset=UTF-8

< 
* Connection #0 to host mercury.picoctf.net left intact
```
## Notas adicionales

## Referencias
