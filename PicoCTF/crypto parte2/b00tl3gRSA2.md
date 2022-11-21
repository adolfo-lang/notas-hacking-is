## b00tl3gRSA2

# objetivo
- In RSA d is a lot bigger than e, why don't we use d to encrypt instead of e? Connect with `nc jupiter.challenges.picoctf.org 57464`.

# Hints
- What is e generally?

# solucion
``` bash 
(kali㉿kali)-[~]
└─$ nc jupiter.challenges.picoctf.org 57464
c: 69848405892907374860652801294755941124321905922231439273559322953709406257081615425425089436334352595123823392470883594914152274142153391903502701598577100516021360529711873487871007346291891379816108916843217098675948999036831608369359688487222206926735272314219939494039923867315155400291415136124502455150
n: 70664136778840296267506652466357331010833038184018625539231932068389953941181471987073467633624264288078267497765949439372128146186703463376545885532277067366901093200229718049643025616777453299801110235564252645239399456046587447210780670733887550818243817818868961880084882575165456404951061115344612927913
e: 21454674361434978945188937100806844568008236473833141751676716729432584700575688993984891877471590259001500933374229243703962736359964989460404199617334463660851446586496277606880139761337536472730927548858979002851019295093624093690184754516322917173309976641770133203048069660501381433696225499047932415745
e = 65537

m = pow(c, e, n)
>>> m
180638594769037903267909311328535969949661653320322151351464061
>>> print(long_to_bytes(m))
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'long_to_bytes' is not defined
>>> from Crypto.Util.number import long_to_bytes
>>> print(long_to_bytes(m))
b'picoCTF{bad_1d3a5_2152720}'


```
# bandera
- picoCTF{bad_1d3a5_2152720}