## credstuff

# objetivo
- We found a leak of a blackmarket website's login credentials. Can you find the password of the user `cultiris` and successfully decrypt it? Download the leak [here](https://artifacts.picoctf.net/c/534/leak.tar). The first user in `usernames.txt` corresponds to the first password in `passwords.txt`. The second user corresponds to the second password, and so on.

# Hints
- Maybe other passwords will have hints about the leak?

# solucion
``` bash 
(kali㉿kali)-[~/basic]
└─$ wget https://artifacts.picoctf.net/c/534/leak.tar   
--2022-11-05 19:12:53--  https://artifacts.picoctf.net/c/534/leak.tar
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.249.74.17, 13.249.74.69, 13.249.74.22, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.249.74.17|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 30720 (30K) [application/octet-stream]
Saving to: ‘leak.tar’

leak.tar       100%  30.00K  51.4KB/s    in 0.6s        

2022-11-05 19:12:56 (51.4 KB/s) - ‘leak.tar’ saved [30720/30720]

                                                         
┌──(kali㉿kali)-[~/basic]
└─$ ls
leak.tar
(kali㉿kali)-[~/basic]
└─$ tar -xvf leak.tar 
leak/
leak/passwords.txt
leak/usernames.txt
                                                         
┌──(kali㉿kali)-[~/basic]
└─$ cd leak    
                                                         
┌──(kali㉿kali)-[~/basic/leak]
└─$ cat passwords.txt | grep {
cvpbPGS{P7e1S_54I35_71Z3}
utilice cesar cipher decoder para decodificar la bandera.
```
# bandera
- picoCTF{C7r1F_54V35_71M3}