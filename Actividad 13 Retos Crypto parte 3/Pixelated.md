## Nombre del reto:
Pixelated

## Objetivo:
I have these 2 images, can you make a flag out of them? [scrambled1.png](https://mercury.picoctf.net/static/6e4afb967ef8c865f79f3a8cd7767cca/scrambled1.png) [scrambled2.png](https://mercury.picoctf.net/static/6e4afb967ef8c865f79f3a8cd7767cca/scrambled2.png)

## Solución:
``┌──(kali㉿kali)-[~]
└─$ mkdir pixel
                                                                             
``┌──(kali㉿kali)-[~]
└─$ cd pixel 
                                                                             
``┌──(kali㉿kali)-[~/pixel]
└─$ wget https://mercury.picoctf.net/static/6e4afb967ef8c865f79f3a8cd7767cca/scrambled1.png
--2022-11-25 03:04:49--  https://mercury.picoctf.net/static/6e4afb967ef8c865f79f3a8cd7767cca/scrambled1.png
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 197171 (193K) [application/octet-stream]
Saving to: ‘scrambled1.png’

scrambled1.png      100%[================>] 192.55K   173KB/s    in 1.1s    

2022-11-25 03:04:51 (173 KB/s) - ‘scrambled1.png’ saved [197171/197171]

                                                                             
``┌──(kali㉿kali)-[~/pixel]
└─$ wget https://mercury.picoctf.net/static/6e4afb967ef8c865f79f3a8cd7767cca/scrambled2.png
--2022-11-25 03:05:04--  https://mercury.picoctf.net/static/6e4afb967ef8c865f79f3a8cd7767cca/scrambled2.png
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 197173 (193K) [application/octet-stream]
Saving to: ‘scrambled2.png’

scrambled2.png      100%[================>] 192.55K   363KB/s    in 0.5s    

2022-11-25 03:05:06 (363 KB/s) - ‘scrambled2.png’ saved [197173/197173]

                                                                             
``┌──(kali㉿kali)-[~/pixel]
└─$ sudo chmod +x stegsolve.jar 
chmod: cannot access 'stegsolve.jar': No such file or directory
                                                                             
``┌──(kali㉿kali)-[~/pixel]
└─$ java -jar stegsolve.jar
Error: Unable to access jarfile stegsolve.jar
                                                                             
``┌──(kali㉿kali)-[~/pixel]
└─$ sudo wget http://www.caesum.com/handbook/Stegsolve.jar -O stegsolve.jar
--2022-11-25 03:05:37--  http://www.caesum.com/handbook/Stegsolve.jar
Resolving www.caesum.com (www.caesum.com)... 216.234.173.1
Connecting to www.caesum.com (www.caesum.com)|216.234.173.1|:80... connected.
HTTP request sent, awaiting response... 200 OK
Length: 312271 (305K) [application/x-java-archive]
Saving to: ‘stegsolve.jar’

stegsolve.jar       100%[================>] 304.95K   116KB/s    in 2.6s    

2022-11-25 03:05:41 (116 KB/s) - ‘stegsolve.jar’ saved [312271/312271]

                                                                             
``┌──(kali㉿kali)-[~/pixel]
└─$ sudo chmod +x stegsolve.jar                                            
                                                                             
``┌──(kali㉿kali)-[~/pixel]
└─$ java -jar stegsolve.jar                                                
Picked up _JAVA_OPTIONS: -Dawt.useSystemAAFontSettings=on -Dswing.aatext=true

Juntamos las dos imagenes y en el apartado de ADD es donde encontramos nuestra bandera:

==picoCTF{0542dc1d}==

## Referencias: