# Bandit Level 22 → Level 23

## Objetivo
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**NOTE:** Looking at shell scripts written by other people is a very useful skill. The script for this level is intentionally made easy to read. If you are having problems understanding what it does, try executing it to see the debug information it prints.

## Datos de Acceso
ssh bandit22@bandit.labs.overthewire.org -p 2220.
WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff

## Solución 
```bash
-  .ls /etc/cron.d -la
		total 48
		drwxr-xr-x   2 root root 4096 Sep  1 06:30 .
		drwxr-xr-x 110 root root 4096 Sep  1 06:30 ..
		-rw-r--r--   1 root root   62 Sep  1 06:30 cronjob_bandit15_root
		-rw-r--r--   1 root root   62 Sep  1 06:30 cronjob_bandit17_root
		-rw-r--r--   1 root root  120 Sep  1 06:30 cronjob_bandit22
		-rw-r--r--   1 root root  122 Sep  1 06:30 cronjob_bandit23
		-rw-r--r--   1 root root  120 Sep  1 06:30 cronjob_bandit24
		-rw-r--r--   1 root root   62 Sep  1 06:30 cronjob_bandit25_root
		-rw-r--r--   1 root root  201 Jan  8  2022 e2scrub_all
		-rwx------   1 root root   52 Sep  1 06:30 otw-tmp-dir
		-rw-r--r--   1 root root  102 Mar 23 13:49 .placeholder
		-rw-r--r--   1 root root  396 Feb  2  2021 sysstat

- cat /etc/cron.d/cronjob_bandit23
		@reboot bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
		* * * * * bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null

- cat /usr/bin/cronjob_bandit23.sh
     #!/bin/bash

	myname=$(whoami)
	mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)
	
	echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"
	
	cat /etc/bandit_pass/$myname > /tmp/$mytarget
	
- echo I am user $myname | md5sum
       7db97df393f40ad1691b6e1fb03d53eb  -

- echo I am user $myname | md5sum | cut -d ' ' -f 1
       7db97df393f40ad1691b6e1fb03d53eb

- myname=bandit23

- echo I am user $myname | md5sum | cut -d ' ' -f 1
     8ca319486bfbbc3663ea0fbe81326349

- cat /tmp/8ca319486bfbbc3663ea0fbe81326349
      QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G
      
```

## Notas Adicionales

## Referencias