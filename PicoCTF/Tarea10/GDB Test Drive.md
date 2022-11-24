## GDB Test Drive

# objetivo
- Can you get the flag? Download this [binary](https://artifacts.picoctf.net/c/115/gdbme). Here's the test drive instructions:

-   `$ chmod +x gdbme`
-   `$ gdb gdbme`
-   `(gdb) layout asm`
-   `(gdb) break *(main+99)`
-   `(gdb) run`
-   `(gdb) jump *(main+104)`

# Hints
- 

# solucion
``` bash 
kali㉿kali)-[~/reversing]
└─$ wget https://artifacts.picoctf.net/c/115/gdbme
--2022-11-23 18:27:14--  https://artifacts.picoctf.net/c/115/gdbme
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 65.9.149.123, 65.9.149.62, 65.9.149.85, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|65.9.149.123|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 17048 (17K) [application/octet-stream]
Saving to: ‘gdbme’

gdbme          100%  16.65K  --.-KB/s    in 0.001s      

2022-11-23 18:27:15 (26.3 MB/s) - ‘gdbme’ saved [17048/17048]

                                                         
┌──(kali㉿kali)-[~/reversing]
└─$ chmod +x gdbme

(kali㉿kali)-[~/reversing]
└─$ gdb gdbme
GNU gdb (Debian 12.1-4) 12.1
Copyright (C) 2022 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.
Type "show copying" and "show warranty" for details.
This GDB was configured as "x86_64-linux-gnu".
Type "show configuration" for configuration details.
For bug reporting instructions, please see:
<https://www.gnu.org/software/gdb/bugs/>.
Find the GDB manual and other documentation resources online at:
    <http://www.gnu.org/software/gdb/documentation/>.

For help, type "help".
Type "apropos word" to search for commands related to "word"...
Reading symbols from gdbme...
(No debugging symbols found in gdbme)
(gdb) layout asm

```
![[Pasted image 20221124170853.png]]

# bandera
- picoCTF{d3bugg3r_dr1v3_197c378a}