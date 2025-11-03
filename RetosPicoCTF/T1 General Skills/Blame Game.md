## Descripción
Someone's commits seems to be preventing the program from working. Who is it?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/72/challenge.zip)
## Solución
```
FRAY30-picoctf@webshell:~/blga$ ls
challenge.zip  drop-in
FRAY30-picoctf@webshell:~/blga$ cd drop-in/
FRAY30-picoctf@webshell:~/blga/drop-in$ ls 
message.py
FRAY30-picoctf@webshell:~/blga/drop-in$ cat message.py 
print("Hello, World!"
FRAY30-picoctf@webshell:~/blga/drop-in$ git log
picoCTF{@sk_th3_1nt3rn_b64c4705}
```
## Notas adicionales

## Referencias
