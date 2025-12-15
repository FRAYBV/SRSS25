## Descripción
In RSA, a small e value can be problematic, but what about N? Can you decrypt this?[values](https://challenge-files.picoctf.net/c_wily_courier/748a8bfc7244df64f48a6ad1d79b5900ee905dd28ebbcd5856652b0e4435393f/values)
## Solución
```
wget https://challenge-files.picoctf.net/c_wily_courier/748a8bfc7244df64f48a6ad1d79b5900ee905dd28ebbcd5856652b0e4435393f/values
--2025-12-15 12:43:15--  https://challenge-files.picoctf.net/c_wily_courier/748a8bfc7244df64f48a6ad1d79b5900ee905dd28ebbcd5856652b0e4435393f/values
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.160.5.40, 3.160.5.64, 3.160.5.18, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.160.5.40|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 205 [application/octet-stream]
Saving to: 'values'

values            100%[===========>]     205  --.-KB/s    in 0s      

2025-12-15 12:43:15 (74.8 MB/s) - 'values' saved [205/205]

FRAY30-picoctf@webshell:/tmp/...mypaq$ ls
values
FRAY30-picoctf@webshell:/tmp/...mypaq$ cat values
Decrypt my super sick RSA:
c: 15341890103764929939105506004034128738090325640037083301857608662849501626260517
n: 948406957756830799684818171639547165784816468744946013083947881743680617123566349
e: 65537
```
rsa cypher: }19ea7cd1_do0g_0n_N_11ams{FTCocip
## Notas adicionales

## Referencias
