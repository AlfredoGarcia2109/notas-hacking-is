## Nombre del reto:
credstuff

## Objetivo:
We found a leak of a blackmarket website's login credentials. Can you find the password of the user `cultiris` and successfully decrypt it?Download the leak [here](https://artifacts.picoctf.net/c/534/leak.tar).The first user in `usernames.txt` corresponds to the first password in `passwords.txt`. The second user corresponds to the second password, and so on.

## Solución:
``┌──(kali㉿kali)-[~]
└─$ mkdir cred
                                                                             
``┌──(kali㉿kali)-[~]
└─$ cd cred 
                                                                             
``┌──(kali㉿kali)-[~/cred]
└─$ wget https://artifacts.picoctf.net/c/534/leak.tar
--2022-11-23 13:34:46--  https://artifacts.picoctf.net/c/534/leak.tar
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.249.74.22, 13.249.74.17, 13.249.74.69, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.249.74.22|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 30720 (30K) [application/octet-stream]
Saving to: ‘leak.tar’

leak.tar            100%[================>]  30.00K  --.-KB/s    in 0.03s   

2022-11-23 13:34:47 (1.07 MB/s) - ‘leak.tar’ saved [30720/30720]

                                                                             
``┌──(kali㉿kali)-[~/cred]
└─$ ls    
^[[B^[[B^[[B^[[B^[[B^[[Bleak.tar
                                                                             
``┌──(kali㉿kali)-[~/cred]
└─$ tar -xvf leak.tar 
leak/
leak/passwords.txt
leak/usernames.txt
                                                                             
``┌──(kali㉿kali)-[~/cred]
└─$ cd leak 
                                                                             
``┌──(kali㉿kali)-[~/cred/leak]
└─$ cat passwords.txt | grep {
cvpbPGS{P7e1S_54I35_71Z3}

*con ayuda de Caesar Cipher decodificamos el passwords para obtener la bandera: **==picoCTF{C7r1F_54V35_71M3}==

## Referencias: