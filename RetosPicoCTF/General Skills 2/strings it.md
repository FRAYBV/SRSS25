## Descripción
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/fae9ac5267cd6e44124e559b901df177/strings) without running it?
## Solución
```
mkdir strit
cd strit/
pwd
wget https://jupiter.challenges.picoctf.org/static/fae9ac5267cd6e44124e559b901df177/strings
ls -la
strings strings
FRAY30-picoctf@webshell:~/strit$ strings strings | grep picoCTF
picoCTF{5tRIng5_1T_7f766a23}
FRAY30-picoctf@webshell:~/strit$
```
## Notas adicionales

## Referencias