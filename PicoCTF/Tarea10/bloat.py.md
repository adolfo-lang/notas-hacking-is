## bloat.py

# objetivo
- Can you get the flag? Run this [Python program](https://artifacts.picoctf.net/c/428/bloat.flag.py) in the same directory as this [encrypted flag](https://artifacts.picoctf.net/c/428/flag.txt.enc).

# Hints
- 

# solucion
``` bash 
(kali㉿kali)-[~/reversing]
└─$ wget https://artifacts.picoctf.net/c/428/bloat.flag.py   
--2022-11-24 16:39:43--  https://artifacts.picoctf.net/c/428/bloat.flag.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 65.9.149.123, 65.9.149.62, 65.9.149.85, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|65.9.149.123|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1557 (1.5K) [application/octet-stream]
Saving to: ‘bloat.flag.py’

bloat.flag.py  100%   1.52K  --.-KB/s    in 0s          

2022-11-24 16:39:44 (16.8 MB/s) - ‘bloat.flag.py’ saved [1557/1557]

                                                         
┌──(kali㉿kali)-[~/reversing]
└─$ wget https://artifacts.picoctf.net/c/428/flag.txt.enc 
--2022-11-24 16:39:58--  https://artifacts.picoctf.net/c/428/flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 65.9.149.57, 65.9.149.85, 65.9.149.62, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|65.9.149.57|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 35 [application/octet-stream]
Saving to: ‘flag.txt.enc’

flag.txt.enc   100%      35  --.-KB/s    in 0s          

2022-11-24 16:39:59 (18.8 MB/s) - ‘flag.txt.enc’ saved [35/35]

                                                         
┌──(kali㉿kali)-[~/reversing]
└─$ ls
bloat.flag.py  flag.txt.enc  gdbme
                                                         
┌──(kali㉿kali)-[~/reversing]
└─$ python3 ./bloat.flag.py ./flag.txt.enc  
Please enter correct password for flag: poqwajoǵeqa
That password is incorrect
                                                         
┌──(kali㉿kali)-[~/reversing]
└─$ code bloat.flag.py
def arg133(arg432):

if arg432 == a[71]+a[64]+a[79]+a[79]+a[88]+a[66]+a[71]+a[64]+a[77]+a[66]+a[68]:

return True

else:

print(a[51]+a[71]+a[64]+a[83]+a[94]+a[79]+a[64]+a[82]+a[82]+a[86]+a[78]+\

a[81]+a[67]+a[94]+a[72]+a[82]+a[94]+a[72]+a[77]+a[66]+a[78]+a[81]+\

a[81]+a[68]+a[66]+a[83])

sys.exit(0)

return False
solo comentamos el sis.exit
sys.exit(0)

(kali㉿kali)-[~/reversing]
└─$ python3 ./bloat.flag.py ./flag.txt.enc
Please enter correct password for flag: 
That password is incorrect
Welcome back... your flag, user:
picoCTF{d30bfu5c4710n_f7w_b8062eec}

```
# bandera
- picoCTF{d30bfu5c4710n_f7w_b8062eec}