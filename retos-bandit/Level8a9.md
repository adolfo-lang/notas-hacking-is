# Bandit Level 8 → Level 9

Objetivo
The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once,

Datos de Acceso
bandit0
bandit0

Solución 
cat data.txt | sort | uniq -u
UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR

Notas Adicionales
con sort se ordena, con uniq y -u muestra las lineas unicas.

Referencias