## Nombre del reto:
Irish-Name-Repo 2

## Objetivo:
There is a website running at https://jupiter.challenges.picoctf.org/problem/53751/ (link). Someone has bypassed the login before, and now it's being strengthened. Try to see if you can still login! or http://jupiter.challenges.picoctf.org:53751

## Solución:

Intentamos la misma inyeccion que el problema pasado, pero detecta una secuencia sql
entonces para omitir la parte del password hacemos la inyeccion en el username
la inyeccion que utilizamos es:
admin´;

Logged in!

Your flag is: ==picoCTF{m0R3_SQL_plz_c34df170}==

## Referencias: