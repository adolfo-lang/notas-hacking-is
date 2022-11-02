## Trivial Flag Transfer Protocol arch

# objetivo
- Figure out how they moved the [flag](https://mercury.picoctf.net/static/b686a99ec088f10b324cfe963bd32dab/tftp.pcapng).

# Hints
- What are some other ways to hide data?

# solucion
``` bash 
(kali㉿kali)-[~]
└─$ mkdir trivial  
                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ cd trivial 
                                                                                                                                                                      
┌──(kali㉿kali)-[~/trivial]
└─$ wget https://mercury.picoctf.net/static/b686a99ec088f10b324cfe963bd32dab/tftp.pcapng              
--2022-11-01 11:26:13--  https://mercury.picoctf.net/static/b686a99ec088f10b324cfe963bd32dab/tftp.pcapng
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 52116496 (50M) [application/octet-stream]
Saving to: ‘tftp.pcapng’

tftp.pcapng                               100%[===================================================================================>]  49.70M   886KB/s    in 54s     

2022-11-01 11:27:16 (936 KB/s) - ‘tftp.pcapng’ saved [52116496/52116496]

                                                                                                                                                                      
┌──(kali㉿kali)-[~/trivial]
└─$ file tftp.pcapng            
tftp.pcapng: pcapng capture file - version 1.0
                                                                                                                                                                      
┌──(kali㉿kali)-[~/trivial]
└─$ wireshark tftp.pcapng                                                               
 ** (wireshark:19269) 11:29:44.338824 [GUI WARNING] -- FIX Add drag reordering to UAT dialog
                                                                                                                                                                      
┌──(kali㉿kali)-[~/trivial]
└─$ wireshark tftp.pcapng
kali㉿kali)-[~/trivial]
└─$ ls
instructions.txt  picture1.bmp  picture2.bmp  picture3.bmp  plan  program.deb  tftp.pcapng
                                                                                                                                                                      
┌──(kali㉿kali)-[~/trivial]
└─$ cat instructions.txt      
GSGCQBRFAGRAPELCGBHEGENSSVPFBJRZHFGQVFTHVFRBHESYNTGENAFSRE.SVTHERBHGNJNLGBUVQRGURSYNTNAQVJVYYPURPXONPXSBEGURCYNA
                                                                                                                                                                      
┌──(kali㉿kali)-[~/trivial]
└─$ cat plan                
VHFRQGURCEBTENZNAQUVQVGJVGU-QHRQVYVTRAPR.PURPXBHGGURCUBGBF
                                                                                                                                                                      
┌──(kali㉿kali)-[~/trivial]
└─$ file program.deb 
program.deb: Debian binary package (format 2.0), with control.tar.gz, data compression xz
(kali㉿kali)-[~/trivial]
└─$ dpkg -I program.deb
 new Debian package, version 2.0.
 size 138310 bytes: control archive=1250 bytes.
     826 bytes,    18 lines      control              
    1184 bytes,    17 lines      md5sums              
 Package: steghide
 Source: steghide (0.5.1-9.1)
 Version: 0.5.1-9.1+b1
 Architecture: amd64
 Maintainer: Ola Lundqvist <opal@debian.org>
 Installed-Size: 426
 Depends: libc6 (>= 2.2.5), libgcc1 (>= 1:4.1.1), libjpeg62-turbo (>= 1:1.3.1), libmcrypt4, libmhash2, libstdc++6 (>= 4.9), zlib1g (>= 1:1.1.4)
 Section: misc
 Priority: optional
 Description: A steganography hiding tool
  Steghide is steganography program which hides bits of a data file
  in some of the least significant bits of another file in such a way
  that the existence of the data file is not visible and cannot be proven.
  .
  Steghide is designed to be portable and configurable and features hiding
  data in bmp, wav and au files, blowfish encryption, MD5 hashing of
  passphrases to blowfish keys, and pseudo-random distribution of hidden bits
  in the container data.
                                                                                                                                                                      
┌──(kali㉿kali)-[~/trivial]
└─$ sudo dpkg -i program.deb
[sudo] password for kali: 
Selecting previously unselected package steghide.
(Reading database ... 353818 files and directories currently installed.)
Preparing to unpack program.deb ...
Unpacking steghide (0.5.1-9.1+b1) ...
(kali㉿kali)-[~/trivial]
└─$ cd flag.txt

```
# bandera
- picoCTF{h1dd3n_1n_pLa1n_51GHT_18375919}