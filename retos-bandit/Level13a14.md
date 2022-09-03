# Bandit Level 13 → Level 14

## Objetivo

The password for the next level is stored in **/etc/bandit_pass/bandit14 and can only be read by user bandit14**. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. **Note:** **localhost** is a hostname that refers to the machine you are working on

## Datos de Acceso
- bandit0
- bandit0

## Solución  
- ls -la
- file sshkey.private
- cat sshkey.private
- chmod 600 llave14
- ssh -i sshkey.private bandit14@localhost
- cat /etc/bandit_pass/bandit14
- fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq

## Notas Adicionales
- chmod cambia los permisos de un archivo

## Referencias