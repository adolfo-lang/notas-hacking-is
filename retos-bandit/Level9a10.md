# Bandit Level 9 → Level 10

## Objetivo
The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.

## Datos de Acceso
bandit0
bandit0

## Solución  
- file data.txt
- cat data.txt | strings | grep ==
- G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s

## Notas Adicionales
- con el strings lo hace legible y con grep filtramos

## Referencias