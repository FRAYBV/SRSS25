## Descripción
We found this [packet capture](https://challenge-files.picoctf.net/c_fickle_tempest/134d2a2cf6ec5b7e757effc9b32977af7cc324b8e99a5ddb64737794a14dc18d/capture.pcap). Recover the flag.
## Solución
```
wget https://challenge-files.picoctf.net/c_fickle_tempest/134d2a2cf6ec5b7e757effc9b32977af7cc324b8e99a5ddb64737794a14dc18d/capture.pcap
--2025-12-14 21:04:35--  https://challenge-files.picoctf.net/c_fickle_tempest/134d2a2cf6ec5b7e757effc9b32977af7cc324b8e99a5ddb64737794a14dc18d/capture.pcap
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.160.5.40, 3.160.5.64, 3.160.5.18, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.160.5.40|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 239455 (234K) [application/octet-stream]
Saving to: 'capture.pcap'

capture.pcap      100%[===========>] 233.84K  --.-KB/s    in 0.1s    

2025-12-14 21:04:35 (1.95 MB/s) - 'capture.pcap' saved [239455/239455]

FRAY30-picoctf@webshell:~$ ls
JWT           colve       flag.txt.en  pw.txt      serpentine
README.txt    cvm         fxm1         pwc1        someta
bigzip        ende.py     fxm2         pwc2        strit
blga          extensions  garden       pwc3        tabtab
bsh           file        index.html   reps        tima
capture.pcap  firstfind   jwt.txt      rupy        waf
cbok          fixme2.py   output.txt   saan        whatlieswithin
cmis          flag        programa.py  salida.txt
FRAY30-picoctf@webshell:~$ file capture.pcap 
capture.pcap: pcap capture file, microsecond ts (little-endian) - version 2.4 (Ethernet, capture length 262144)
FRAY30-picoctf@webshell:~$ xdg-open capture.pcap
```
## Notas adicionales

## Referencias
