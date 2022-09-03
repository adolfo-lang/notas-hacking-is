# Bandit Level 18 → Level 19

## Objetivo
The password for the next level is stored in a file **readme** in the homedirectory. Unfortunately, someone has modified **.bashrc** to log you out when you log in with SSH.

## Datos de Acceso
- bandit0.
- bandit0

## Solución 
- ssh bandit18@bandit.labs.overthewire.org -p 2220 "/bin/bash"
- ls -la
- cat readme
awhqfNnAbc1naukrpqDYcF95h7HoMTrC

## Notas Adicionales
- /bin/bash ejecuta el bash sin prompt

## Referencias