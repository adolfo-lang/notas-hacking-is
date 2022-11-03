## Lookey here

# objetivo
- Attackers have hidden information in a very large mass of data in the past, maybe they are still doing it. Download the data [here](https://artifacts.picoctf.net/c/294/anthem.flag.txt).

# Hints
- Download the file and search for the flag based on the known prefix.

# solucion
``` bash 
kali㉿kali)-[~]
└─$ mkdir look
                                                            
┌──(kali㉿kali)-[~]
└─$ cd look    
                                                            
┌──(kali㉿kali)-[~/look]
└─$ wget https://artifacts.picoctf.net/c/294/anthem.flag.txt 
--2022-11-03 11:23:39--  https://artifacts.picoctf.net/c/294/anthem.flag.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.249.74.17, 13.249.74.69, 13.249.74.22, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.249.74.17|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 108668 (106K) [application/octet-stream]
Saving to: ‘anthem.flag.txt’

anthem.flag.tx 100%[====>] 106.12K  --.-KB/s    in 0.1s    

2022-11-03 11:23:40 (808 KB/s) - ‘anthem.flag.txt’ saved [108668/108668]

                                                            
┌──(kali㉿kali)-[~/look]
└─$ file anthem.flag.txt       
anthem.flag.txt: Unicode text, UTF-8 text
                                                            
┌──(kali㉿kali)-[~/look]
└─$ cat anthem.flag.txt      
      ANTHEM

      by Ayn Rand


        CONTENTS

         PART ONE

         PART TWO

         PART THREE

         PART FOUR

         PART FIVE

         PART SIX

         PART SEVEN

         PART EIGHT

         PART NINE

         PART TEN

         PART ELEVEN

         PART TWELVE




      PART ONE

      It is a sin to write this. It is a sin to think words no others
      think and to put them down upon a paper no others are to see. It
(kali㉿kali)-[~/look]
└─$ cat anthem.flag.txt | grep pico
      we think that the men of picoCTF{gr3p_15_@w3s0m3_4c479940}

```
# bandera
- picoCTF{gr3p_15_@w3s0m3_4c479940}