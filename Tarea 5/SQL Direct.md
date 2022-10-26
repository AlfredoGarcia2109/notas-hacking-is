## Nombre del reto: SQL Direct


### Objetivo:
Connect to this PostgreSQL server and find the flag!`psql -h saturn.picoctf.net -p 51445 -U postgres pico`Password is `postgres`


### Solución:
``┌──(kali㉿kali)-[~]
└─$ psql -h saturn.picoctf.net -p 63823 -U postgres pico
Password for user postgres: 
psql (14.4 (Debian 14.4-1+b1), server 14.2 (Debian 14.2-1.pgdg110+1))
Type "help" for help.

``pico=# \l
``pico=# \l
``pico=# \dt
         List of relations
 Schema | Name  | Type  |  Owner   
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)

``pico=# select * from flags
``pico-# select * from flags;
ERROR:  syntax error at or near "select"
LINE 2: select * from flags;
        ^
``pico=# SELECT * FROM flags;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_21c94904}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)

==picoCTF{L3arN_S0m3_5qL_t0d4Y_21c94904}

### Referencias: