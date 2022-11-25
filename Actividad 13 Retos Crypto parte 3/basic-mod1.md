## Nombre del reto:
basic-mod1

## Objetivo:
We found this weird message being passed around on the servers, we think we have a working decryption scheme.Download the message [here](https://artifacts.picoctf.net/c/394/message.txt).Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore.Wrap your decrypted message in the picoCTF flag format (i.e. `picoCTF{decrypted_message}`)

## Solución:
``┌──(kali㉿kali)-[~]
└─$ mkdir basicmod
                                                                             
``┌──(kali㉿kali)-[~]
└─$ cd basicmod   
                                                                             
``┌──(kali㉿kali)-[~/basicmod]
└─$ wget https://artifacts.picoctf.net/c/394/message.txt
--2022-11-23 13:12:14--  https://artifacts.picoctf.net/c/394/message.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 65.9.149.123, 65.9.149.57, 65.9.149.85, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|65.9.149.123|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 86 [application/octet-stream]
Saving to: ‘message.txt’

message.txt         100%[================>]      86  --.-KB/s    in 0s      

2022-11-23 13:12:17 (36.6 MB/s) - ‘message.txt’ saved [86/86]

                                                                             
``┌──(kali㉿kali)-[~/basicmod]
└─$ cat message.txt 
202 137 390 235 114 369 198 110 350 396 390 383 225 258 38 291 75 324 401 142 288 397                                                                              
``┌──(kali㉿kali)-[~/basicmod]
└─$ nano flag.py   
                                                                             
``┌──(kali㉿kali)-[~/basicmod]
└─$ nano flag.py
                                                                             
``┌──(kali㉿kali)-[~/basicmod]
└─$ python3 flag.py   
  File "/home/kali/basicmod/flag.py", line 1
    x=[202 137 390 235 114 369 198 110 350 396 390 383 225 258 38 291 75 324 401 142 288 397]
       ^^^^^^^
SyntaxError: invalid syntax. Perhaps you forgot a comma?
                                                                             
``┌──(kali㉿kali)-[~/basicmod]
└─$ nano flag.py   
                                                                             
``┌──(kali㉿kali)-[~/basicmod]
└─$ nano flag.py
                                                                             
``┌──(kali㉿kali)-[~/basicmod]
└─$ 
                                                                             
``┌──(kali㉿kali)-[~/basicmod]
└─$ python3 flag.py
  File "/home/kali/basicmod/flag.py", line 1
    x=[202 137 390 235 114 369 198 110 350 396 390 383 225 258 38 291 75 324 401 142 288 397]
       ^^^^^^^
SyntaxError: invalid syntax. Perhaps you forgot a comma?
                                                                             
``┌──(kali㉿kali)-[~/basicmod]
└─$ nano flag.py   
                                                                             
``┌──(kali㉿kali)-[~/basicmod]
└─$ python3 flag.py
==R0UND_N_R0UND_B6B25531==

## Referencias: