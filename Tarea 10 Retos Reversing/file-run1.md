## Nombre del reto:
file-run1

## Objetivo:
A program has been provided to you, what happens if you try to run it on the command line?Download the program [here](https://artifacts.picoctf.net/c/310/run).

## Solución:
``┌──(kali㉿kali)-[~]
└─$ mkdir run1 
                                                                             
``┌──(kali㉿kali)-[~]
└─$ cd run1 
                                                                             
``┌──(kali㉿kali)-[~/run1]
└─$ wget https://artifacts.picoctf.net/c/310/run         
--2022-11-25 13:07:50--  https://artifacts.picoctf.net/c/310/run
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.249.74.69, 13.249.74.17, 13.249.74.56, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.249.74.69|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16736 (16K) [application/octet-stream]
Saving to: ‘run’

run                 100%[================>]  16.34K  61.5KB/s    in 0.3s    

2022-11-25 13:07:52 (61.5 KB/s) - ‘run’ saved [16736/16736]

                                                                             
``┌──(kali㉿kali)-[~/run1]
└─$ ls
run
                                                                             
``┌──(kali㉿kali)-[~/run1]
└─$ file run  
run: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, BuildID[sha1]=0514683255a9ef58abe3c729e7418d07210a759e, for GNU/Linux 3.2.0, not stripped
                                                                             
``┌──(kali㉿kali)-[~/run1]
└─$ ls -la
total 28
drwxr-xr-x  2 kali kali  4096 Nov 25 13:07 .
drwxr-xr-x 59 kali kali  4096 Nov 25 13:07 ..
-rw-r--r--  1 kali kali 16736 Mar 15  2022 run
                                                                             
``┌──(kali㉿kali)-[~/run1]
└─$ chmod +x run  
                                                                             
``┌──(kali㉿kali)-[~/run1]
└─$ ./run  
The flag is: ==picoCTF{U51N6_Y0Ur_F1r57_F113_47cf2b7b}==

## Referencias: