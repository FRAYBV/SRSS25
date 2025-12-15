## Descripción
We found this weird message being passed around on the servers, we think we have a working decryption scheme.Download the message [here](https://artifacts.picoctf.net/c/127/message.txt).Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore.Wrap your decrypted message in the picoCTF flag format (i.e. `picoCTF{decrypted_message}`)
## Solución
```
numeros = [128, 322, 353, 235, 336, 73, 198, 332, 202, 285, 57, 87, 262, 221, 218, 405, 335, 101, 2]

  

caracteres = "ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789_"

  

mensaje_descifrado = ''.join([caracteres[numero % 37] for numero in numeros])

  

print(f"picoCTF{{{mensaje_descifrado}}}")
```
picoCTF{R0UND_N_R0UND_79C1C}
## Notas adicionales

## Referencias
