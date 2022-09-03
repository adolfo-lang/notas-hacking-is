# Bandit Level 10 → Level 11

## Objetivo
The password for the next level is stored in the file **data.txt**, which contains base64 encoded data

## Datos de Acceso
ssh bandit10@bandit.labs.overthewire.org -p 2220
- G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s

## Solución  
- ls
    data.txt
- cat data.txt | base64 -d
     The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
- 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM

## Notas Adicionales
- con base 64 -d hcemos legible el contenido del archivo

## Referencias