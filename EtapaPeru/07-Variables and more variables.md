# Variables and more variables

## Objetivo
Considere un sistema RSA con p=7, q= 11 and = e=13, encuentre el texto plano correspondiente a c=17. Encuentra el valor de m

## Solucion
```python
──(kali㉿kali)-[~]
└─$ python3        
Python 3.10.5 (main, Jun  8 2022, 09:26:22) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> from Crypto.Util.number import inverse
>>> p = 7
>>> q = 11
>>> e = 13
>>> c = 17
>>> n = p * q
>>> tn = (p-1) * (q-1)
>>> d=inverse(e,tn)
>>> m = pow(c,d,n)
>>> m
52
>>> 
```

```bandera
52
```
