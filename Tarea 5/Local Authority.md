## Nombre del reto: Local Authority


### Objetivo:
Can you get the flag?Go to this [website](http://saturn.picoctf.net:55826/) and see what you can discover.


### Solución:
Nos metemos al codifo fuente e ingresamos al login.php, ya ahi ingresamos al secure.js donde podemos observar el usuario y a contraseña if( username === 'admin' && password === 'strongPassword098765' ), solo ingresamos con los datos que se nos dio y obtenemos la bandera

==picoCTF{j5_15_7r4n5p4r3n7_b0c2c9cb}== 

### Referencias: