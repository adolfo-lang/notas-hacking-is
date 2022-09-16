# Bandit Level 32 → Level 33

## Objetivo
After all this `git` stuff its time for another escape. Good luck!

## Datos de Acceso
- ssh bandit32@bandit.labs.overthewire.org -p 2220
- rmCBvG56y58BXzv98yZGdO7ATVL5dW8y

## Solución
``` bash
WELCOME TO THE UPPERCASE SHELL
>> ls -la
sh: 1: LS: not found
>> $SHELL
WELCOME TO THE UPPERCASE SHELL
>> $EUID
>> $0
$ export SHELL=/bin/bash
$ echo $SHELL
/bin/bash
$ $SHELL
bandit33@bandit:~$ cat /etc/bandit_pass/bandit33
odHo63fHiFqcWWJG9rLiLDtPm45KzUKy
```
## Notas Adicionales


## Referencias
