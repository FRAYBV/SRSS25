## Descripción
Can you get the flag?
Go to this [website](http://saturn.picoctf.net:57296/) and see what you can discover.
## Solución
Al acceder vemos el codigo fuente
[secure.js](http://saturn.picoctf.net:57296/secure.js)
```
function checkPassword(username, password)
{
  if( username === 'admin' && password === 'strongPassword098765' )
  {
    return true;
  }
  else
  {
    return false;
  }
}
```
Ingresamos los datos en el login
picoCTF{j5_15_7r4n5p4r3n7_05df90c8}
## Notas adicionales

## Referencias
