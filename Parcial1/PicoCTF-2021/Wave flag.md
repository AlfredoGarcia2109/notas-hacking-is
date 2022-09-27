

# Nombre del reto:
Wave a flag

# Objetivo:
Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/a00f554b16385d9970dae424f66ee1ab/warm) has extraordinarily helpful information...
# Solución:
┌──(kali㉿kali)-[~/Downloads]
``└─$ ls -la
total 828
drwxr-xr-x  3 kali kali   4096 Sep 26 23:46 .
drwxr-xr-x 17 kali kali   4096 Sep 26 23:44 ..
drwxr-xr-x  3 kali kali   4096 Mar 15  2021 Addadshashanammu
-rw-r--r--  1 kali kali   4520 Sep 26 23:14 Addadshashanammu.zip
-rw-r--r--  1 kali kali  14551 Sep 26 19:36 file
-rw-r--r--  1 kali kali     34 Sep 26 23:43 flag
-rw-r--r--  1 kali kali    785 Sep 26 23:02 ltdis.sh
-rw-r--r--  1 kali kali   8376 Sep 26 23:02 static
-rw-r--r--  1 kali kali 776032 Sep 26 19:29 strings
-rw-r--r--  1 kali kali  10936 Sep 26 23:46 warm
                                                                             
┌──(kali㉿kali)-[~/Downloads]
``└─$ strings -d warm| grep pico 
Oh, help? I actually don't do much, but I do have this flag here: ==picoCTF{b1scu1ts_4nd_gr4vy_18788aaa}

# Referencias: