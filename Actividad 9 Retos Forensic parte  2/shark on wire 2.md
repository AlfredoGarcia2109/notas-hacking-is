## Nombre del reto:
shark on wire 2

## Objetivo:
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap). Recover the flag that was pilfered from the network.

## Solución:
``┌──(kali㉿kali)-[~]
└─$ mkdir shark2 
                                                                             
``┌──(kali㉿kali)-[~]
└─$ cd shark2 
                                                                             
``┌──(kali㉿kali)-[~/shark2]
└─$ wget https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap
--2022-11-24 17:23:07--  https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 112318 (110K) [application/octet-stream]
Saving to: ‘capture.pcap’

capture.pcap        100%[================>] 109.69K   272KB/s    in 0.4s    

2022-11-24 17:23:11 (272 KB/s) - ‘capture.pcap’ saved [112318/112318]

                                                                             
``┌──(kali㉿kali)-[~/shark2]
└─$ ls
capture.pcap

en la info tenemos el puerto origen, de ahi vamos sacando los numeros restando 5000:
112 105 99 111 67 84 70 123 112 049 076 076 102 051 114 051 100 95 100 97 116 97 95 118 049 097 095 115 116 051 103 048 125 

con ayuda de un convertidor de ascii a texto convertimos esos numeros y asi obtenemos la bandera:
==picoCTF{p1LLf3r3d_data_v1a_st3g0}==

https://www.duplichecker.com/ascii-to-text.php

## Referencias: