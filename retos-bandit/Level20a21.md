# Bandit Level 20 → Level 21

## Objetivo
There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

**NOTE:** Try connecting to your own network daemon to see if it works as you think

## Datos de Acceso
bandit0
bandit0

## Solución 
- ls -la
- nc -lnvp 3050 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT &
- ./suconnect 3050
NvEJF7oVjkddltPSrdKEFOllh9V1IBcq

Notas Adicionales
- se abre una conexion en el puerto 3050 y se pone en escucha el puerto y se ejecuta en segundo plano con el &

## Referencias