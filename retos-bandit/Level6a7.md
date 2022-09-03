# Bandit Level 6 → Level 7

## Objetivo
The password for the next level is stored **somewhere on the server** and has all of the following properties:

-   owned by user bandit7
-   owned by group bandit6
-   33 bytes in size

## Datos de Acceso
bandit0
bandit0

## Solución  
ls
find / -user bandit7 -group  bandit6 -size 33c 2>/dev/null
cat /var/lib/dpkg/info/bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S

## Notas Adicionales
la salida estandar de error 2 la manda a null y no las muestra en pantalla 2>/dev/null

## Referencias