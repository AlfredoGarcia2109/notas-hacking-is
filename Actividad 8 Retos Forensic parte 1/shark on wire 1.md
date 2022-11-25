## Nombre del reto:
shark on wire 1

## Objetivo:
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap). Recover the flag.

## Solución:
``┌──(kali㉿kali)-[~]
└─$ mkdir shark1 
                                                                             
``┌──(kali㉿kali)-[~]
└─$ cd shark1 
                                                                             
``┌──(kali㉿kali)-[~/shark1]
└─$ wget https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap
--2022-11-24 12:20:00--  https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 239455 (234K) [application/octet-stream]
Saving to: ‘capture.pcap’

capture.pcap        100%[================>] 233.84K   143KB/s    in 1.6s    

2022-11-24 12:20:04 (143 KB/s) - ‘capture.pcap’ saved [239455/239455]

                                                                             
``┌──(kali㉿kali)-[~/shark1]
└─$ file capture.pcap 
capture.pcap: pcap capture file, microsecond ts (little-endian) - version 2.4 (Ethernet, capture length 262144)
                                                                             
``┌──(kali㉿kali)-[~/shark1]
└─$ wireshark capture.pcap 
^C
                                                                             
``┌──(kali㉿kali)-[~/shark1]
└─$ 
                                                                             
``┌──(kali㉿kali)-[~/shark1]
└─$ wireshark capture.pcap

dentro del wireshark seguimos(follow) los protocolos UDP hasta llegar al stream 6 donde ahi encontramos la bandera

==picoCTF{StaT31355_636f6e6e}==

## Referencias: