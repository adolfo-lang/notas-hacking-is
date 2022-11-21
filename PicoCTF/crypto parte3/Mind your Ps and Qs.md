## Mind your Ps and Qs

# objetivo
- In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/3cfeb09681369c26e3f19d886bc1e5d9/values)

# Hints
- Bits are expensive, I used only a little bit over 100 to save money

# solucion
``` bash 
(kali㉿kali)-[~]
└─$ cd crypto
                                                         
┌──(kali㉿kali)-[~/crypto]
└─$ wget https://mercury.picoctf.net/static/3cfeb09681369c26e3f19d886bc1e5d9/values
--2022-11-20 20:27:42--  https://mercury.picoctf.net/static/3cfeb09681369c26e3f19d886bc1e5d9/values
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 203 [application/octet-stream]
Saving to: ‘values’

values         100%     203  --.-KB/s    in 0s          

2022-11-20 20:27:44 (49.8 MB/s) - ‘values’ saved [203/203]

                                                         
┌──(kali㉿kali)-[~/crypto]
└─$ cat values    
Decrypt my super sick RSA:
c: 8533139361076999596208540806559574687666062896040360148742851107661304651861689
n: 769457290801263793712740792519696786147248001937382943813345728685422050738403253
e: 65537
81 [(show)](http://factordb.com/index.php?showid=1100000002524298763)

[7694572908...53](http://factordb.com/index.php?id=1100000002524298763)<81> = [1617549722683965197900599011412144490161](http://factordb.com/index.php?id=1100000002524306701)<40> · [475693130177488446807040098678772442581573](http://factordb.com/index.php?id=1100000002524306700)<42>
(kali㉿kali)-[~]
└─$ python3
Python 3.10.7 (main, Sep  8 2022, 14:34:29) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> from Crypto.Util.number import long_to_bytes
>>> from Crypto.Util.number import inverse
>>> 
>>> c = 8533139361076999596208540806559574687666062896040360148742851107661304651861689
>>> e = 65537
>>> p = 1617549722683965197900599011412144490161
>>> q = 475693130177488446807040098678772442581573
>>> n = p*q
>>> n
769457290801263793712740792519696786147248001937382943813345728685422050738403253
>>> tn = (p-1)*(q-1)
>>> d = inverse(e,tn)
>>> m = pow(c, d, n)
>>> m
13016382529449106065927291425342535437996222135352905256639629442503647501498237
>>> print(long_to_bytes(m))
>>> b'picoCTF{sma11_N_n0_g0od_45369387}'
```
# bandera
- picoCTF{sma11_N_n0_g0od_45369387}