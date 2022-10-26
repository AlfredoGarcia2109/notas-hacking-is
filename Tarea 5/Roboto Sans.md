## Nombre del reto: Roboto Sans


### Objetivo:

The flag is somewhere on this web application not necessarily on the website. Find it.Check [this](http://saturn.picoctf.net:64710/) out.

### Solución:
solo agregamos el robots.txt en el link y despues copiamos anMvbXlmaWxlLnR4dA==
que es el nombre del archivo pero encriptado, con ayuda de la consola desencriptamos el texto

``┌──(kali㉿kali)-[~]
└─$ echo anMvbXlmaWxlLnR4dA== | base64 -d     
js/myfile.txt                                                                             

en el link de la pagina quitamos el robots.txt y ponemos myfile.txt y ahi obtenemos la bandera``

==picoCTF{Who_D03sN7_L1k5_90B0T5_032f1c2b}==

### Referencias: