## Nombre del reto:
Sleuthkit Intro

## Objetivo:
Download the disk image and use `mmls` on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

-   [Download disk image](https://artifacts.picoctf.net/c/114/disk.img.gz)
-   Access checker program: `nc saturn.picoctf.net 52279`

## Solución:
``┌──(kali㉿kali)-[~]
└─$ mkdir sleuthkit   
                                                                             
``┌──(kali㉿kali)-[~]
└─$ cd sleuthkit 
                                                                             
``┌──(kali㉿kali)-[~/sleuthkit]
└─$ wget https://artifacts.picoctf.net/c/114/disk.img.gz  
--2022-11-24 21:30:53--  https://artifacts.picoctf.net/c/114/disk.img.gz
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.249.74.17, 13.249.74.56, 13.249.74.69, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.249.74.17|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 29714372 (28M) [application/octet-stream]
Saving to: ‘disk.img.gz’

disk.img.gz         100%[================>]  28.34M   329KB/s    in 7m 43s  

2022-11-24 21:38:37 (62.7 KB/s) - ‘disk.img.gz’ saved [29714372/29714372]

                                                                             
``┌──(kali㉿kali)-[~/sleuthkit]
└─$ gzip -d disk.img.gz
                                                                             
``┌──(kali㉿kali)-[~/sleuthkit]
└─$ ls -la
total 102408
drwxr-xr-x  2 kali kali      4096 Nov 24 21:38 .
drwxr-xr-x 40 kali kali      4096 Nov 24 21:30 ..
-rw-r--r--  1 kali kali 104857600 Mar 15  2022 disk.img
                                                                             
``┌──(kali㉿kali)-[~/sleuthkit]
└─$ mmls disk.img  
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000204799   0000202752   Linux (0x83)
                                                                             
``┌──(kali㉿kali)-[~/sleuthkit]
└─$ nc saturn.picoctf.net 52279
What is the size of the Linux partition in the given disk image?
Length in sectors: 202752                     
202752
Great work!
==picoCTF{mm15_f7w!}==

## Referencias: