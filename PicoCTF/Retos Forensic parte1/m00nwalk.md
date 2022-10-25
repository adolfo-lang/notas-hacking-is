## m00nwalk

# objetivo
- Decode this [message](https://jupiter.challenges.picoctf.org/static/fc1edf07742e98a480c6aff7d2546107/message.wav) from the moon.

# Hints
- How did pictures from the moon landing get sent back to Earth?
- What is the CMU mascot?, that might help select a RX option

# solucion
``` bash 
(kali㉿kali)-[~/Downloads]
└─$ mkdir moon
                                                           
┌──(kali㉿kali)-[~/Downloads]
└─$ cd moon
                                                           
┌──(kali㉿kali)-[~/Downloads/moon]
└─$ wget https://jupiter.challenges.picoctf.org/static/fc1edf07742e98a480c6aff7d2546107/message.wav  
--2022-10-25 12:48:00--  https://jupiter.challenges.picoctf.org/static/fc1edf07742e98a480c6aff7d2546107/message.wav
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 11066998 (11M) [application/octet-stream]
Saving to: ‘message.wav’

message.wav    100%  10.55M  3.11MB/s    in 4.0s          

2022-10-25 12:48:05 (2.61 MB/s) - ‘message.wav’ saved [11066998/11066998]

                                                           
┌──(kali㉿kali)-[~/Downloads/moon]
└─$ ls
message.wav
                                                           
┌──(kali㉿kali)-[~/Downloads/moon]
└─$ open message.wav
(kali㉿kali)-[~/Downloads/moon]
└─$ mkdir moonrepo                             
                                                           
┌──(kali㉿kali)-[~/Downloads/moon]
└─$ cd moonrepo 
                                                           
┌──(kali㉿kali)-[~/Downloads/moon/moonrepo]
└─$ sudo git clone https://github.com/colaclanth/sstv.git
[sudo] password for kali: 
Cloning into 'sstv'...
remote: Enumerating objects: 221, done.
remote: Total 221 (delta 0), reused 0 (delta 0), pack-reused 221
Receiving objects: 100% (221/221), 1.01 MiB | 1.74 MiB/s, done.
Resolving deltas: 100% (140/140), done.
                                                           
┌──(kali㉿kali)-[~/Downloads/moon/moonrepo]
└─$ sudo python3 setup.py install                       
python3: cant open file /home/kali/Downloads/moon/moonrepo/setup.py: [Errno 2] No such file or directory
(kali㉿kali)-[~/Downloads/moon/moonrepo/sstv]
└─$ sudo python3 setup.py install
running install
/usr/lib/python3/dist-packages/setuptools/command/install.py:34: SetuptoolsDeprecationWarning: setup.py install is deprecated. Use build and pip and other standards-based tools.
  warnings.warn(
/usr/lib/python3/dist-packages/setuptools/command/easy_install.py:158: EasyInstallDeprecationWarning: easy_install command is deprecated. Use build and pip and other standards-based tools.
  warnings.warn(
running bdist_egg
running egg_info
creating sstv.egg-info
writing sstv.egg-info/PKG-INFO
(kali㉿kali)-[~/Downloads/moon]
└─$ sstv -d message.wav -o result.png
[sstv] Searching for calibration header... Found!    
[sstv] Detected SSTV mode Scottie 1
[sstv] Decoding image...   [#########################] 100%
[sstv] Drawing image data...
[sstv] ...Done!
                                                           
┌──(kali㉿kali)-[~/Downloads/moon]
└─$ open result.png 

```
# bandera
- picoCTF{beep_boop_im_in_space}


























## Glory of the Garden

# objetivo
- This [garden](https://jupiter.challenges.picoctf.org/static/4153422e18d40363e7ffc7e15a108683/garden.jpg) contains more than it seems.

# Hints
- What is a hex editor?

# solucion
``` bash 


```
# bandera
- picoCTF{more_than_m33ts_the_3y33dd2eEF5}