## Wireshark twoo twooo two twoo.

# objetivo
- Can you find the flag? [shark2.pcapng](https://mercury.picoctf.net/static/0fe13a33318e756f71c35cb490e64c81/shark2.pcapng).

# Hints
- Did you really find _the_ flag?
- Look for traffic that seems suspicious.

# solucion
``` bash 
(kali㉿kali)-[~]
└─$ mkdir wrieshark
                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ cd wrieshark
                                                                                                                                                                      
┌──(kali㉿kali)-[~/wrieshark]
└─$ wget https://mercury.picoctf.net/static/0fe13a33318e756f71c35cb490e64c81/shark2.pcapng
--2022-11-02 11:02:53--  https://mercury.picoctf.net/static/0fe13a33318e756f71c35cb490e64c81/shark2.pcapng
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 3520112 (3.4M) [application/octet-stream]
Saving to: ‘shark2.pcapng’

shark2.pcapng                             100%[===================================================================================>]   3.36M  3.00MB/s    in 1.1s    

2022-11-02 11:03:03 (3.00 MB/s) - ‘shark2.pcapng’ saved [3520112/3520112]

                                                                                                                                                                      
┌──(kali㉿kali)-[~/wrieshark]
└─$ ls
shark2.pcapng
                                                                                                                                                                      
┌──(kali㉿kali)-[~/wrieshark]
└─$ file shark2.pcapng 
shark2.pcapng: pcapng capture file - version 1.0
                                                                                                                                                                      
┌──(kali㉿kali)-[~/wrieshark]
└─$ wireshark shark2.pcapng                                                               
 ** (wireshark:48385) 11:31:06.534203 [GUI WARNING] -- QXcbConnection: XCB error: 3 (BadWindow), sequence: 16438, resource id: 22137367, major code: 40 (TranslateCoords), minor code: 0
                                                                                                                                                                      
┌──(kali㉿kali)-[~/wrieshark]
└─$ nano data.csv 
                                                                                                                                                                      
┌──(kali㉿kali)-[~/wrieshark]
└─$ cat data.csv | cut -d ' ' -f 5
cGljb0NU.reddshrimpandherring.com.windomain.local"
RntkbnNf.reddshrimpandherring.com.windomain.local"
M3hmMWxf.reddshrimpandherring.com.windomain.local"
ZnR3X2Rl.reddshrimpandherring.com.windomain.local"
YWRiZWVm.reddshrimpandherring.com.windomain.local"
fQ==.reddshrimpandherring.com.windomain.local"
                                                                                                                                                                      
┌──(kali㉿kali)-[~/wrieshark]
└─$ cat data.csv | cut -d ' ' -f 5 | cut -d '.' -f1
cGljb0NU
RntkbnNf
M3hmMWxf
ZnR3X2Rl
YWRiZWVm
fQ==
                                                                                                                                                                      
┌──(kali㉿kali)-[~/wrieshark]
└─$ cat data.csv | cut -d ' ' -f 5 | cut -d '.' -f1 | tr -d '\n' | base64 -d
picoCTF{dns_3xf1l_ftw_deadbeef}

```
# bandera
- picoCTF{dns_3xf1l_ftw_deadbeef}