## ## cesar

# objetivo
- Decrypt this [message](https://jupiter.challenges.picoctf.org/static/7d707a443e95054dc4cf30b1d9522ef0/ciphertext).
# Hints
- caesar cipher [tutorial](https://learncryptography.com/classical-encryption/caesar-cipher)

# solucion
``` bash 
(kali㉿kali)-[~/crypto]
└─$ wget https://jupiter.challenges.picoctf.org/static/7d707a443e95054dc4cf30b1d9522ef0/ciphertext
--2022-11-16 11:21:40--  https://jupiter.challenges.picoctf.org/static/7d707a443e95054dc4cf30b1d9522ef0/ciphertext
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 35 [application/octet-stream]
Saving to: ‘ciphertext’

ciphertext     100%      35  --.-KB/s    in 0s          

2022-11-16 11:21:41 (26.8 MB/s) - ‘ciphertext’ saved [35/35]

                                                         
┌──(kali㉿kali)-[~/crypto]
└─$ file ciphertext  
ciphertext: ASCII text, with no line terminators
                                                         
┌──(kali㉿kali)-[~/crypto]
└─$ cat ciphertext 
picoCTF{gvswwmrkxlivyfmgsrhnrisegl}
{crossingtherubicondjneoach}
```
# bandera
- picoCTF{crossingtherubicondjneoach}