## basic-mod1

# objetivo
- We found this weird message being passed around on the servers, we think we have a working decryption scheme. Download the message [here](https://artifacts.picoctf.net/c/393/message.txt). Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore. Wrap your decrypted message in the picoCTF flag format (i.e. `picoCTF{decrypted_message}`)

# Hints
- Do you know what `mod 37` means?
- `mod 37` means modulo 37. It gives the remainder of a number after being divided by 37.

# solucion
``` bash 
(kali㉿kali)-[~]
└─$ mkdir basic
                                                         
┌──(kali㉿kali)-[~]
└─$ cd basic      
                                                         
┌──(kali㉿kali)-[~/basic]
└─$ wget https://artifacts.picoctf.net/c/393/message.txt
--2022-11-05 18:20:00--  https://artifacts.picoctf.net/c/393/message.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.249.74.56, 13.249.74.17, 13.249.74.69, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.249.74.56|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 84 [application/octet-stream]
Saving to: ‘message.txt’

message.txt    100%      84  --.-KB/s    in 0s          

2022-11-05 18:20:00 (27.4 MB/s) - ‘message.txt’ saved [84/84]

                                                         
┌──(kali㉿kali)-[~/basic]
└─$ cat message.txt 
54 396 131 198 225 258 87 258 128 211 57 235 114 258 144 220 39 175 330 338 297 288
(kali㉿kali)-[~/basic]
└─$ nano solucion.py
x=[4,396,131,198,225,258,87,258,128,211,57,235,114,258,1>
y=x
for i in range(len(x)):
  y[i]=x[i]%37

s=""
for i in range(len(y)):
   if y[i]<26:
      s+=chr(ord('A')+y[i])
   elif y[i]<36:
      s+=chr(ord('0')+y[i]-26)
   else:
      s+="_"
print(s)
(kali㉿kali)-[~/basic]
└─$ python3 solucion.py
E0UND_N_R0UND_79C18FB3
```
# bandera
- picoCTF{R0UND_N_R0UND_79C18FB3}