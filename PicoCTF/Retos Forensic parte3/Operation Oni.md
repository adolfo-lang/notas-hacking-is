## Operation Oni

# objetivo
- Download this disk image, find the key and log into the remote machine. Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

# Hints
- 

# solucion
``` bash 

(kali㉿kali)-[~]
└─$ mkdir operation
                                                                                                                                                                     
┌──(kali㉿kali)-[~]
└─$ cd operation
(kali㉿kali)-[~/operation]
└─$ wget https://artifacts.picoctf.net/c/373/disk.img.gz
--2022-11-02 12:26:10--  https://artifacts.picoctf.net/c/373/disk.img.gz
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.249.74.69, 13.249.74.56, 13.249.74.22, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.249.74.69|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 48132743 (46M) [application/octet-stream]
Saving to: ‘disk.img.gz’

disk.img.gz                               100%[==================================================================================>]  45.90M  7.29MB/s    in 7.4s    

2022-11-02 12:26:18 (6.17 MB/s) - ‘disk.img.gz’ saved [48132743/48132743]

                                                                                                                                                                     
┌──(kali㉿kali)-[~/operation]
└─$ gzip -d disk.img.gz
(kali㉿kali)-[~/operation]
└─$ gzip -d disk.img.gz
                                                                                                                                                                     
┌──(kali㉿kali)-[~/operation]
└─$ ls -la
total 235528
drwxr-xr-x  2 kali kali      4096 Nov  2 12:26 .
drwxr-xr-x 29 kali kali      4096 Nov  2 12:21 ..
-rw-r--r--  1 kali kali 241172480 Mar 15  2022 disk.img
                                                                                                                                                                     
┌──(kali㉿kali)-[~/operation]
└─$ mmls disk.img  
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000471039   0000264192   Linux (0x83)
                                                                                                                                                                     
┌──(kali㉿kali)-[~/operation]
└─$ fls -o 206848 disk.img                         
d/d 458:        home
d/d 11: lost+found
d/d 12: boot
d/d 13: etc
d/d 79: proc
d/d 80: dev
d/d 81: tmp
d/d 82: lib
d/d 85: var
d/d 94: usr
d/d 104:        bin
d/d 118:        sbin
d/d 464:        media
d/d 468:        mnt
d/d 469:        opt
d/d 470:        root
d/d 471:        run
d/d 473:        srv
d/d 474:        sys
V/V 33049:      $OrphanFiles
                                                                                                                                                                     
┌──(kali㉿kali)-[~/operation]
└─$ fls -o 206848 disk.img 470                     
r/r 2344:       .ash_history
d/d 3916:       .ssh
                                                                                                                                                                     
┌──(kali㉿kali)-[~/operation]
└─$ fls -o 206848 disk.img 3916                    
r/r 2345:       id_ed25519
r/r 2346:       id_ed25519.pub
kali㉿kali)-[~/operation]
└─$ icat -o 206848 disk.img 2345 > key_file
                                                                                                                                                                     
┌──(kali㉿kali)-[~/operation]
└─$ chmod 400 key_file                                    
                                                                                                                                                                     
┌──(kali㉿kali)-[~/operation]
└─$ ssh -i key_file -p 64869 ctf-player@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:64869 ([18.217.86.78]:64869)' cant be established.
ED25519 key fingerprint is SHA256:5gIm/EJ9bYnoH4qed83W5HXLfN1DO55849f6Lze0lx8.
This host key is known by the following other names/addresses:
    ~/.ssh/known_hosts:3: [hashed name]
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:64869' (ED25519) to the list of known hosts.
Welcome to Ubuntu 20.04.3 LTS (GNU/Linux 5.13.0-1025-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

ctf-player@challenge:~$ ls
flag.txt
ctf-player@challenge:~$ cat flag.txt    
picoCTF{k3y_5l3u7h_b5066e83}ctf-player@challenge:~$ 

```
# bandera
- picoCTF{k3y_5l3u7h_b5066e83}