Bandit Level 0 → Level 1

Objetivo
The password for the next level is stored in a file called **readme** located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

Datos de acceso
boJ9jbbUNNfktd78OOpsqOltutMc3MY1

Solución
bandit0@bandit:~$ pwd
/home/bandit0
bandit0@bandit:~$ ls
readme
bandit0@bandit:~$ cat readme
boJ9jbbUNNfktd78OOpsqOltutMc3MY1

Notas adicionales
pwd - en que directorio estoy
ls - listar archivos
cat - mostrar archivos

Referencias