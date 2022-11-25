## Nombre del reto:
file-run2

## Objetivo:
Another program, but this time, it seems to want some input. What happens if you try to run it on the command line with input "Hello!"?Download the program [here](https://artifacts.picoctf.net/c/353/run).

## Solución:
``┌──(kali㉿kali)-[~]
└─$ mkdir run2
                                                                             
``┌──(kali㉿kali)-[~]
└─$ cd run2 
                                                                             
``┌──(kali㉿kali)-[~/run2]
└─$ wget https://artifacts.picoctf.net/c/353/run
--2022-11-25 13:09:54--  https://artifacts.picoctf.net/c/353/run
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 99.84.192.17, 99.84.192.11, 99.84.192.79, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|99.84.192.17|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16816 (16K) [application/octet-stream]
Saving to: ‘run’

run                 100%[================>]  16.42K  --.-KB/s    in 0s      

2022-11-25 13:09:56 (65.9 MB/s) - ‘run’ saved [16816/16816]

                                                                             
``┌──(kali㉿kali)-[~/run2]
└─$ ls -la
total 28
drwxr-xr-x  2 kali kali  4096 Nov 25 13:09 .
drwxr-xr-x 60 kali kali  4096 Nov 25 13:09 ..
-rw-r--r--  1 kali kali 16816 Mar 15  2022 run
                                                                             
``┌──(kali㉿kali)-[~/run2]
└─$ chmod +x run
                                                                             
``┌──(kali㉿kali)-[~/run2]
└─$ ./run
Run this file with only one argument.
                                                                             
``┌──(kali㉿kali)-[~/run2]
└─$ ./run Hello!
The flag is: ==picoCTF{F1r57_4rgum3n7_f65ed63e}==

## Referencias: