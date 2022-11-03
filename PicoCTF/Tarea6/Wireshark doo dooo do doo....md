## Wireshark doo dooo do doo...

# objetivo
- Can you find the flag? [shark1.pcapng](https://mercury.picoctf.net/static/b44842413a0834f4a3619e5f5e629d05/shark1.pcapng).

# Hints
- 

# solucion
``` bash 
(kali㉿kali)-[~]
└─$ mkdir doo        
                                                            
┌──(kali㉿kali)-[~]
└─$ cd doo      
                                                            
┌──(kali㉿kali)-[~/doo]
└─$ wget https://mercury.picoctf.net/static/b44842413a0834f4a3619e5f5e629d05/shark1.pcapng
--2022-11-03 10:59:26--  https://mercury.picoctf.net/static/b44842413a0834f4a3619e5f5e629d05/shark1.pcapng
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1558808 (1.5M) [application/octet-stream]
Saving to: ‘shark1.pcapng’

shark1.pcapng  100%[====>]   1.49M  2.01MB/s    in 0.7s    

2022-11-03 10:59:27 (2.01 MB/s) - ‘shark1.pcapng’ saved [1558808/1558808]

                                                            
┌──(kali㉿kali)-[~/doo]
└─$ wireshark shark1.pcapng

Gur synt vf cvpbPGS{c33xno00_1_f33_h_qrnqorrs}
(kali㉿kali)-[~/doo]
└─$ echo "cvpbPGS{c33xno00_1_f33_h_qrnqorrs}" | tr 'A-Za-z' 'N-ZA-Mn-za-m'
picoCTF{p33kab00_1_s33_u_deadbeef}
```
# bandera
- picoCTF{p33kab00_1_s33_u_deadbeef}