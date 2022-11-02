## Sleuthkit Intr

# objetivo
- Download the disk image and use `mmls` on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag. Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

# Hints
- 

# solucion
``` bash 

(kali㉿kali)-[~]
└─$ mkdir sleu     
                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ cd sleu
                                                                                                                                                                      
┌──(kali㉿kali)-[~/sleu]
└─$ wgethttps://artifacts.picoctf.net/c/114/disk.img.gz                                   
zsh: no such file or directory: wgethttps://artifacts.picoctf.net/c/114/disk.img.gz
                                                                                                                                                                      
┌──(kali㉿kali)-[~/sleu]
└─$ wget https://artifacts.picoctf.net/c/114/disk.img.gz
--2022-11-02 11:43:31--  https://artifacts.picoctf.net/c/114/disk.img.gz
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 65.9.121.39, 65.9.121.65, 65.9.121.3, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|65.9.121.39|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 29714372 (28M) [application/octet-stream]
Saving to: ‘disk.img.gz’

disk.img.gz                               100%[===================================================================================>]  28.34M  2.73MB/s    in 9.7s    

2022-11-02 11:43:49 (2.94 MB/s) - ‘disk.img.gz’ saved [29714372/29714372]

                                                                                                                                                                      
┌──(kali㉿kali)-[~/sleu]
└─$ gzip -d disk.img.gz                        
                                                                                                                                                                      
┌──(kali㉿kali)-[~/sleu]
└─$ ls -la
total 102408
drwxr-xr-x  2 kali kali      4096 Nov  2 11:45 .
drwxr-xr-x 28 kali kali      4096 Nov  2 11:43 ..
-rw-r--r--  1 kali kali 104857600 Mar 15  2022 disk.img
                                                                                                                                                                      
┌──(kali㉿kali)-[~/sleu]
└─$ mmls disk.img  
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000204799   0000202752   Linux (0x83)
                                                                                                                                                                      
┌──(kali㉿kali)-[~/sleu]
└─$ ns saturn.picoctf.net 202752
ns: command not found
                                                                                                                                                                      
┌──(kali㉿kali)-[~/sleu]
└─$ nc saturn.picoctf.net 202752
saturn.picoctf.net [18.217.86.78] 6144 (?) : Connection refused
                                                                                                                                                                      
┌──(kali㉿kali)-[~/sleu]
└─$ nc saturn.picoctf.net 52279
What is the size of the Linux partition in the given disk image?
Length in sectors: 202752                     
202752
Great work!
picoCTF{mm15_f7w!}
```
# bandera
- picoCTF{mm15_f7w!}