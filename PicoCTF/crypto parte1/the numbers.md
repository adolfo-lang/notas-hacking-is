## the numbers

# objetivo
- The [numbers](https://jupiter.challenges.picoctf.org/static/f209a32253affb6f547a585649ba4fda/the_numbers.png)... what do they mean?
# Hints
- The flag is in the format PICOCTF{}

# solucion
``` bash 
(kali㉿kali)-[~]
└─$ mkdir crypto
                                                         
┌──(kali㉿kali)-[~]
└─$ cd crypto 
                                                         
┌──(kali㉿kali)-[~/crypto]
└─$ wget https://jupiter.challenges.picoctf.org/static/f209a32253affb6f547a585649ba4fda/the_numbers.png
--2022-11-16 10:53:24--  https://jupiter.challenges.picoctf.org/static/f209a32253affb6f547a585649ba4fda/the_numbers.png
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 100721 (98K) [application/octet-stream]
Saving to: ‘the_numbers.png’

the_numbers.pn 100%  98.36K   454KB/s    in 0.2s        

2022-11-16 10:53:25 (454 KB/s) - ‘the_numbers.png’ saved [100721/100721]

                                                         
┌──(kali㉿kali)-[~/crypto]
└─$ open the_numbers.png
16 9 3 15 3 20 6 { 20 8 5 14 21 13 2 5 18 19 13 1 19 15 14 }
utilice el cyberchef
picoctf.thenumbersmason.

```
# bandera
- picoCTF{thenumbersmason}