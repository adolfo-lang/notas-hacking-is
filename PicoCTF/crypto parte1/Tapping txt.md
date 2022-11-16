## Tapping txt

# objetivo
- Theres tapping coming in from the wires. What's it saying `nc jupiter.challenges.picoctf.org 48247`.

# Hints
- What kind of encoding uses dashes and dots?
- The flag is in the format PICOCTF{}

# solucion
``` bash 
(kali㉿kali)-[~/crypto]
└─$ nc jupiter.challenges.picoctf.org 48247
.--. .. -.-. --- -.-. - ..-. { -- ----- .-. ... ...-- -.-. ----- -.. ...-- .---- ... ..-. ..- -. .---- ..--- -.... .---- ....- ...-- ---.. .---- ---.. .---- }
se solucionó en cyberchef con codigo morse

PICOCTFM0RS3C0D31SFUN1261438181
```
# bandera
- picoCTF{M0RS3C0D31SFUN1261438181}