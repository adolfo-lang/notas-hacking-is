# Bandit Level 11 → Level 12

## Objetivo
The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

## Datos de Acceso
ssh bandit11@bandit.labs.overthewire.org -p 2220
6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM

## Solución  
- ls
    data.txt
- cat data.txt | tr "["a-zA-Z "]" "["n-za-mN-ZA-M"]"
      The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
- JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv

## Notas Adicionales
tr camnia caracteres lo siguiente son la operaciones

## Referencias