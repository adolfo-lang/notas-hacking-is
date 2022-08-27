# Bandido Nivel 5 → Nivel 6

Objetivo
The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:

-   human-readable
-   1033 bytes in size
-   not executable

Datos de Acceso
bandit0
bandit0

Solución 
ls
cd inhere
ls
find . -size 1033c -type f
cat ./maybehere07/.file2
DXjZPULLxYr17uwoI01bNLQbtFemEgo7

Notas Adicionales
con el comando find se puede hacer una busqueda
-size especificamos el tamaño de archivo
-type especificamos el tipo

Referencias

