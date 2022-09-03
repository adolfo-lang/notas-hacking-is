# Bandit Level 21 → Level 22

## Objetivo
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

## Datos de Acceso
ssh bandit21@bandit.labs.overthewire.org -p 2220.
NvEJF7oVjkddltPSrdKEFOllh9V1IBcq

## Solución 
- man 5 crontab
     CRONTAB(5)                    File Formats Manual                   CRONTAB(5)

	NAME
	       crontab - tables for driving cron
	
	DESCRIPTION.........

- ls -la
     total 24
	drwxr-xr-x  2 root     root     4096 Sep  1 06:30 .
	drwxr-xr-x 49 root     root     4096 Sep  1 06:30 ..
	-rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
	-rw-r--r--  1 root     root     3771 Jan  6  2022 .bashrc
	-r--------  1 bandit21 bandit21   33 Sep  1 06:30 .prevpass
	-rw-r--r--  1 root     root      807 Jan  6  2022 .profile
	
- cat /etc/cron.d/cronjob_bandit22
     @reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
    * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
 
- cat /etc/usr/cronjob_bandit22.sh
      #!/bin/bash
	chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
	cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv

- cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv

WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff

## Notas Adicionales
cron nos ayuda a controlar las tareas que se van a estar ejecutando.

## Referencias