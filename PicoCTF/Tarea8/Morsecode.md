## Morsecode

# objetivo
- Morse code is well known. Can you decrypt this? Download the file [here](https://artifacts.picoctf.net/c/235/morse_chal.wav). Wrap your answer with picoCTF{}, put underscores in place of pauses, and use all lowercase.

# Hints
- Audacity is a really good program to analyze morse code audio.

# solucion
``` bash 
utilice un decodificador de audio
https://morsecode.world/international/decoder/audio-decoder-adaptive.html
W H 4 7 H 4 7 H 9 0 D W 2 0 U 9 H 7
(kali㉿kali)-[~/basic]
└─$ python3            
Python 3.10.7 (main, Sep  8 2022, 14:34:29) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> "W H 4 7 H 4 7 H 9 0 D W 2 0 U 9 H 7".lower().replace(' ','')
'wh47h47h90dw20u9h7'

```
# bandera
- picoCTF{wh47_h47h_90d_w20u9h7}