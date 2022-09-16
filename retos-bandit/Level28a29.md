# Bandit Level 28 → Level 29

## Objetivo

There is a git repository at `ssh://bandit28-git@localhost/home/bandit28-git/repo`. The password for the user `bandit28-git` is the same as for the user `bandit28`.

## Datos de Acceso
- ssh bandit28@bandit.labs.overthewire.org -p 2220
- AVanL161y9rsbcJIsFHuw35rjaOM19nR
 
## Solución
```bash
mkdir /tmp/adolfogit
cd /tmp/adolfogit
 git clone "ssh://bandit28-git@localhost:2220/home/bandit28-git/repo"
     !!! You are trying to log into this SSH server on port 2220 on localhost.
	!!! Please log out and log in again instead.
	
	bandit27-git@localhost's password:
	remote: Enumerating objects: 3, done.
	remote: Counting objects: 100% (3/3), done.
	remote: Compressing objects: 100% (2/2), done.
	remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
	Receiving objects: 100% (3/3), done.
	
bandit28@bandit:/tmp/adolfogit$ ls -la
total 236
drwxrwxr-x    3 bandit28 bandit28   4096 Sep 15 19:42 .
drwxrwx-wt 3542 root     root     229376 Sep 15 19:47 ..
drwxrwxr-x    3 bandit28 bandit28   4096 Sep 15 19:43 repo
bandit28@bandit:/tmp/adolfogit$ cd repo
bandit28@bandit:/tmp/adolfogit/repo$ ls
README.md
bandit28@bandit:/tmp/adolfogit/repo$ cat readme.md
cat: readme.md: No such file or directory
bandit28@bandit:/tmp/adolfogit/repo$ README.MD
README.MD: command not found
bandit28@bandit:/tmp/adolfogit/repo$ cat README.md

Some notes for level29 of bandit.

credentials

- username: bandit29
- password: xxxxxxxxxx

bandit28@bandit:/tmp/adolfogit/repo$ ^C
bandit28@bandit:/tmp/adolfogit/repo$ cd .git
bandit28@bandit:/tmp/adolfogit/repo/.git$ ls -la
total 52
drwxrwxr-x 8 bandit28 bandit28 4096 Sep 15 19:43 .
drwxrwxr-x 3 bandit28 bandit28 4096 Sep 15 19:43 ..
drwxrwxr-x 2 bandit28 bandit28 4096 Sep 15 19:42 branches
-rw-rw-r-- 1 bandit28 bandit28  281 Sep 15 19:43 config
-rw-rw-r-- 1 bandit28 bandit28   73 Sep 15 19:42 description
-rw-rw-r-- 1 bandit28 bandit28   23 Sep 15 19:43 HEAD
drwxrwxr-x 2 bandit28 bandit28 4096 Sep 15 19:42 hooks
-rw-rw-r-- 1 bandit28 bandit28  137 Sep 15 19:43 index
drwxrwxr-x 2 bandit28 bandit28 4096 Sep 15 19:42 info
drwxrwxr-x 3 bandit28 bandit28 4096 Sep 15 19:43 logs
drwxrwxr-x 4 bandit28 bandit28 4096 Sep 15 19:42 objects
-rw-rw-r-- 1 bandit28 bandit28  114 Sep 15 19:43 packed-refs
drwxrwxr-x 5 bandit28 bandit28 4096 Sep 15 19:43 refs
bandit28@bandit:/tmp/adolfogit/repo/.git$ git log
commit 43032edb2fb868dea2ceda9cb3882b2c336c09ec (HEAD -> master, origin/master, origin/HEAD)
Author: Morla Porla <morla@overthewire.org>
Date:   Thu Sep 1 06:30:25 2022 +0000

    fix info leak

commit bdf3099fb1fb05faa29e80ea79d9db1e29d6c9b9
Author: Morla Porla <morla@overthewire.org>
Date:   Thu Sep 1 06:30:25 2022 +0000

    add missing data

commit 43d032b360b700e881e490fbbd2eee9eccd7919e
Author: Ben Dover <noone@overthewire.org>
Date:   Thu Sep 1 06:30:24 2022 +0000

    initial commit of README.md
bandit28@bandit:/tmp/adolfogit/repo/.git$ git show 43032edb2fb868dea2ceda9cb3882b2c336c09ec
commit 43032edb2fb868dea2ceda9cb3882b2c336c09ec (HEAD -> master, origin/master, origin/HEAD)
Author: Morla Porla <morla@overthewire.org>
Date:   Thu Sep 1 06:30:25 2022 +0000

    fix info leak

diff --git a/README.md b/README.md
index b302105..5c6457b 100644
--- a/README.md
+++ b/README.md
@@ -4,5 +4,5 @@ Some notes for level29 of bandit.
 ## credentials

 - username: bandit29
-- password: tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S
+- password: xxxxxxxxxx
```
## Notas Adicionales
- git log muestra las diferencias entre los commits
- git show, para confirmaciones, muestra el mensaje de registro y la diferencia textual.
## Referencias
- https://git-scm.com/docs