# Bandit Level 9 → Level 10

Objetivo
The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.

Datos de Acceso
bandit0
bandit0

Solución 
file data.txt
cat data.txt | strings | grep ==
truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk

Notas Adicionales
con el strings lo hace legible y con grep filtramos

Referencias