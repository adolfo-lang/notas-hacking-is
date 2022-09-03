# Bandit Level 19 → Level 20

## Objetivo
To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.

## Datos de Acceso
- ssh bandit19@bandit.labs.overthewire.org -p 2220..
- awhqfNnAbc1naukrpqDYcF95h7HoMTrC

## Solución 
- ls -la
     total 36
	drwxr-xr-x  2 root     root      4096 Sep  1 06:30 .
	drwxr-xr-x 49 root     root      4096 Sep  1 06:30 ..
	-rw-r--r--  1 root     root       220 Jan  6  2022 .bash_logout
	-rw-r--r--  1 root     root      3771 Jan  6  2022 .bashrc
	-rw-r--r--  1 root     root       807 Jan  6  2022 .profile
	-rwsr-x---  1 bandit20 bandit19 14872 Sep  1 06:30 bandit20-do
	
-  ./bandit20-do id
     uid=11019(bandit19) gid=11019(bandit19) euid=11020(bandit20) groups=11019(bandit19)
-  ./bandit20-do cat /etc/bandit_pass/bandit20
VxCazJaVykI6W36BkBU0mJTCM8rR95XT
## Notas Adicionales
- si esta activdo el bit setuid, podemos ejecutar a nombre de otro usuario

## Referencias