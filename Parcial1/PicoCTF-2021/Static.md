# Nombre del reto:
Static aint always note

# Objetivo:
Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/7495259e963bd5b67d0fb8b616652618/static)? This [BASH script](https://mercury.picoctf.net/static/7495259e963bd5b67d0fb8b616652618/ltdis.sh) might help!
# Solución:#
``┌──(kali㉿kali)-[~]
└─$ cd Downloads 
                                                                             

                                                                             
```┌──(kali㉿kali)-[~/Downloads]
└─$ ls -la
total 800
drwxr-xr-x  2 kali kali   4096 Sep 26 23:03 .
drwxr-xr-x 16 kali kali   4096 Sep 26 22:49 ..
-rw-r--r--  1 kali kali  14551 Sep 26 19:36 file
-rw-r--r--  1 kali kali    785 Sep 26 23:02 ltdis.sh
-rw-r--r--  1 kali kali   8376 Sep 26 23:02 static
-rw-r--r--  1 kali kali 776032 Sep 26 19:29 strings
                                                                             
```
```┌──(kali㉿kali)-[~/Downloads]```
└─$ strings static | grep pico
==picoCTF{d15a5m_t34s3r_ccb2b43e}

# referencias: