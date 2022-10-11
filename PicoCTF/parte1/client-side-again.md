## client-side-again

# objetivo
- Can you break into this super secure portal? `https://jupiter.challenges.picoctf.org/problem/60786/` ([link](https://jupiter.challenges.picoctf.org/problem/60786/)) or http://jupiter.challenges.picoctf.org:60786

# Hints
- What is obfuscation?

# solucion
``` bash 
inspeccionamos el codigo y nos damos cuenta que el
codigo esta ofuscado, usamos jsNIce para desofuscarlo
var _0x5a46 = ["f49bf}", "_again_e", "this", "Password Verified", "Incorrect password", "getElementById", "value", "substring", "picoCTF{", "not_this"];
picoCTF{not_this_again_ef49bf}

```
# bandera
- picoCTF{not_this_again_ef49bf}