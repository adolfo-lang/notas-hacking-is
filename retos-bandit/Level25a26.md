# Bandit Level 25 → Level 26

## Objetivo
Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not **/bin/bash**, but something else. Find out what it is, how it works and how to break out of it

## Datos de Acceso
- ssh bandit25@bandit.labs.overthewire.org -p 2220
- p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d

## Solución 
```bash
- ls -la
		total 32
		drwxr-xr-x  2 root     root     4096 Sep  1 06:30 .
		drwxr-xr-x 49 root     root     4096 Sep  1 06:30 ..
		-rw-r-----  1 bandit25 bandit25   33 Sep  1 06:30 .bandit24.password
		-r--------  1 bandit25 bandit25 1679 Sep  1 06:30 bandit26.sshkey
		-rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
		-rw-r--r--  1 root     root     3771 Jan  6  2022 .bashrc
		-rw-r-----  1 bandit25 bandit25    4 Sep  1 06:30 .pin
		-rw-r--r--  1 root     root      807 Jan  6  2022 .profile

- file bandit26.sshkey
    bandit26.sshkey: PEM RSA private key

-  ssh -i bandit26.sshkey bandit26@localhost -p 2220
		The authenticity of host [localhost]:2220 ([127.0.0.1]:2220) cant be established.
		ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
		Connection to localhost closed.

- cat /etc/passwd | grep bandit26
     bandit26:x:11026:11026:bandit level 26:/home/bandit26:/usr/bin/showtext
- set shell=/bin/bash
- shell
- cat /etc/bandit26_pass/bandit26
c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1
```
## Notas Adicionales
para poder resolver este nivel fue necesario reducir la terminal, loego teclear la 'v' para entrar a modo edicion, y ahi poder indicar para entrar al shell de el usuario bandit26

## Referencias
