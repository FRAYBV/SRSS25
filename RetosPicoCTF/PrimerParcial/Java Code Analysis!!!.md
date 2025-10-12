## Descripción
BookShelf Pico, my premium online book-reading service.I believe that my website is super secure. I challenge you to prove me wrong by reading the 'Flag' book!
Additional details will be available after launching your challenge instance.
## Solución
Se aplica en un token decoder la barrera de administración que se encuentra al inspeccionar el sitio, ahí se modifica el payload a:
{
  "role": "Admin",
  "iss": "bookshelf",
  "exp": 1760903571,
  "iat": 1760298771,
  "userId": 2,
  "email": "admin"
}

Ahora tanto el nuevo payload como el nuevo token se agregan en el almacenamiento local y se recarga la pagina, dejando ver el libro y encontrar la bandera:
picoCTF{w34k_jwt_n0t_g00d_d7c2e335}
## Notas adicionales

## Referencias