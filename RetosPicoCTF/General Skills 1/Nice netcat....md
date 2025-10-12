# Nice netcat...
## Descripción
There is a nice program that you can talk to by using this command in a shell: `$ nc mercury.picoctf.net 43239`, but it doesn't speak English...
## Solución
```bash
nc mercury.picoctf.net 43239 > salida.txt
cat salida.txt

nano programa.py
```

``` python
with open('salida.txt', 'r') as file:
    lines = file.readlines()

lines = [line.strip() for line in lines]

myFlag = ""

for l in lines:
    tempChar = chr(int(l))
    myFlag+=tempChar

print(myFlag)
```

```bash
python3 programa.py
picoCTF{g00d_k1tty!_n1c3_k1tty!_7c0821f5}
```
## Notas adicionales

## Referencias
