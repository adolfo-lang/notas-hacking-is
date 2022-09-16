# Bandit Level 30 → Level 31

## Objetivo

There is a git repository at `ssh://bandit30-git@localhost/home/bandit30-git/repo`. The password for the user `bandit30-git` is the same as for the user `bandit30`.

Clone the repository and find the password for the next level.

## Datos de Acceso
- ssh bandit30@bandit.labs.overthewire.org -p 2220
- xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS

## Solución
```bash
mkdir /tmp/adolfogit4
bandit29@bandit:/$ cd /tmp/adolfogit4
bandit30@bandit:/tmp/adolfogit4$ git clone "ssh://bandit30-git@localhost:2220/home/bandit30-git/repo"
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
bandit30-git@localhost's password:
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (4/4), done.
cd repo
bandit30@bandit:/tmp/adolfogit4/repo$ ls -la
total 16
drwxrwxr-x 3 bandit30 bandit30 4096 Sep 16 04:02 .
drwxrwxr-x 3 bandit30 bandit30 4096 Sep 16 04:02 ..
drwxrwxr-x 8 bandit30 bandit30 4096 Sep 16 04:02 .git
-rw-rw-r-- 1 bandit30 bandit30   30 Sep 16 04:02 README.md
bandit30@bandit:/tmp/adolfogit4/repo$ cat README.md
just an epmty file... muahaha
bandit30@bandit:/tmp/adolfogit4/repo$ git log
commit a325f29e1cc26b0f0dc5f89b4348e389b408cc87 (HEAD -> master, origin/master, origin/HEAD)
Author: Ben Dover <noone@overthewire.org>
Date:   Thu Sep 1 06:30:28 2022 +0000

    initial commit of README.md
bandit30@bandit:/tmp/adolfogit4/repo$ git branch -r
  origin/HEAD -> origin/master
  origin/master
bandit30@bandit:/tmp/adolfogit4/repo$ cat README.md
just an epmty file... muahaha
bandit30@bandit:/tmp/adolfogit4/repo$ git tag
secret
bandit30@bandit:/tmp/adolfogit4/repo$ git show secret
OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt
```
## Notas Adicionales
- git branch enlista las ramas
- git-checkout  Cambiar ramas o restaurar archivos de árbol de trabajo
- git-tag Enumerar las etiquetas existentes en Git
## Referencias
- https://git-scm.com/docs