## unpackme.py

# objetivo
- Can you get the flag? Reverse engineer this [Python program](https://artifacts.picoctf.net/c/464/unpackme.flag.py).

# Hints
- 

# solucion
``` bash 
(kali㉿kali)-[~/reversing]
└─$ wget https://artifacts.picoctf.net/c/464/unpackme.flag.py
--2022-11-24 16:16:48--  https://artifacts.picoctf.net/c/464/unpackme.flag.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 65.9.149.123, 65.9.149.62, 65.9.149.85, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|65.9.149.123|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 527 [application/octet-stream]
Saving to: ‘unpackme.flag.py’

unpackme.flag. 100%     527  --.-KB/s    in 0s          

2022-11-24 16:16:48 (6.54 MB/s) - ‘unpackme.flag.py’ saved [527/527]

                                                         
┌──(kali㉿kali)-[~/reversing]
└─$ code unpackme.flag.py 
                                                         
┌──(kali㉿kali)-[~/reversing]
└─$ python3 unpackme.flag.py            
Whats the password? 
That password is incorrect.


import base64

from cryptography.fernet import Fernet

  
  
  

payload = b'gAAAAABiMD04m0Z6CohVV7ozdwHqtgc2__CuAFGG8rWhZBTL0lhfzp-mhu9LYNMnMQMGO-7tEwy3DJ2Y8yjogvzyojFETwN9YEIPXTnO9F1QnkPypWTgjISGve4gcSerJMs694oKcIdKHuVaSxOg1MMNs5k9iPaBIPU7xOKQqCyhnf_f4yUvLdMcer38BqRptocJNvKlyWN8h7ikoWL0zlssxd8OJyPujMz78HZaefvUouvq6LDtPVqRBJFPgSJYf1nHpHKFa1O0zJ6UpTe6ba3PPAxCVXutNg=='

  

key_str = 'correctstaplecorrectstaplecorrec'

key_base64 = base64.b64encode(key_str.encode())

f = Fernet(key_base64)

plain = f.decrypt(payload)

exec(plain.decode())
se cambio exec por print
print(plain.decode())
(kali㉿kali)-[~/reversing]
└─$ python3 unpackme.flag.py

pw = input('What\'s the password? ')

if pw == 'batteryhorse':
  print('picoCTF{175_chr157m45_5274ff21}')
else:
  print('That password is incorrect.')

```
# bandera
- picoCTF{175_chr157m45_5274ff21}