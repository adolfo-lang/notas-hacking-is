# Bandit Level 27 → Level 28

## Objetivo
There is a git repository at `ssh://bandit27-git@localhost/home/bandit27-git/repo`. The password for the user `bandit27-git` is the same as for the user `bandit27`.

Clone the repository and find the password for the next level.

## Datos de Acceso
- ssh bandit26@bandit.labs.overthewire.org -p 2220
- YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS

## Solución 
```BASH
-  mkdir /tmp/adolfogit
-  cd /tmp/adolfogit
       bandit27@bandit:/tmp/adolfogit$
- git clone "ssh://bandit27-git@localhost:2220/home/bandit27-git/repo"
     !!! You are trying to log into this SSH server on port 2220 on localhost.
	!!! Please log out and log in again instead.
	
	bandit27-git@localhost's password:
	remote: Enumerating objects: 3, done.
	remote: Counting objects: 100% (3/3), done.
	remote: Compressing objects: 100% (2/2), done.
	remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
	Receiving objects: 100% (3/3), done.
- ls -la
	total 236
	drwxrwxr-x    3 bandit27 bandit27   4096 Sep 11 02:24 .
	drwxrwx-wt 3811 root     root     229376 Sep 11 02:23 ..
	drwxrwxr-x    3 bandit27 bandit27   4096 Sep 11 02:24 repo
- cd repo
     bandit27@bandit:/tmp/adolfohrgit/repo$
- ls -la
	total 16
	drwxrwxr-x 3 bandit27 bandit27 4096 Sep 11 02:24 .
	drwxrwxr-x 3 bandit27 bandit27 4096 Sep 11 02:24 ..
	drwxrwxr-x 8 bandit27 bandit27 4096 Sep 11 02:24 .git
	-rw-rw-r-- 1 bandit27 bandit27   68 Sep 11 02:24 README
- cat README
    The password to the next level is: AVanL161y9rsbcJIsFHuw35rjaOM19nR
```
## Notas Adicionales
- en este reto se clono un repositorio
## Referencias