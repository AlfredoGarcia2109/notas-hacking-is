## Nombre del reto:
Packets Primer

## Objetivo:
Download the packet capture file and use packet analysis software to find the flag.

-   [Download packet capture](https://artifacts.picoctf.net/c/201/network-dump.flag.pcap)

## Solución:
``┌──(kali㉿kali)-[~/Downloads]
└─$ wireshark network-dump.flag.pcap 
picoCTF{p4ck37_5h4rk_01b0a0d6}

###### abrimos el network-dump.flag.pcap en el wireshar y el primer tcp seguimos como tcp stream
==p i c o C T F { p 4 c k 3 7 _ 5 h 4 r k _ 0 1 b 0 a 0 d 6 }==, solo le quitamos los espacios para cumplir con el formato de las banderas

## Referencias: