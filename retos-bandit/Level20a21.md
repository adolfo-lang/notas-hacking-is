# Bandit Level 20 → Level 21

## Objetivo
There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

**NOTE:** Try connecting to your own network daemon to see if it works as you think

## Datos de Acceso
ssh bandit20@bandit.labs.overthewire.org -p 2220.
VxCazJaVykI6W36BkBU0mJTCM8rR95XT

## Solución 
- ls -la
     total 36
	drwxr-xr-x  2 root     root      4096 Sep  1 06:30 .
	drwxr-xr-x 49 root     root      4096 Sep  1 06:30 ..
	-rw-r--r--  1 root     root       220 Jan  6  2022 .bash_logout
	-rw-r--r--  1 root     root      3771 Jan  6  2022 .bashrc
	-rw-r--r--  1 root     root       807 Jan  6  2022 .profile
	-rwsr-x---  1 bandit21 bandit20 15596 Sep  1 06:30 suconnect
	
- nc -lnvp 3050 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT &
     [1] 3356068
     bandit20@bandit:~$ Listening on 0.0.0.0 3050
- ./suconnect 3050
     Connection received on 127.0.0.1 36884
	Read: VxCazJaVykI6W36BkBU0mJTCM8rR95XT
	Password matches, sending next password
	NvEJF7oVjkddltPSrdKEFOllh9V1IBcq
	[1]+  Done                    nc -lnvp 3050 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT
	
NvEJF7oVjkddltPSrdKEFOllh9V1IBcq

Notas Adicionales
- se abre una conexion en el puerto 3050 y se pone en escucha el puerto y se ejecuta en segundo plano con el &

## Referencias