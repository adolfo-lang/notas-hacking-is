# Bandit Level 17 → Level 18

## Objetivo
There are 2 files in the homedirectory: **passwords.old and passwords.new**. The password for the next level is in **passwords.new** and is the only line that has been changed between **passwords.old and passwords.new**

**NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19**

## Datos de Acceso
- ssh bandit17@bandit.labs.overthewire.org -p 2220
- VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e

## Solución 
- ls -la
- diff passwords.old passwords.new
hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg

## Notas Adicionales
- diff nos permite comparar un archivo linea a linea

## Referencias