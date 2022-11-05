## Mod 26

# objetivo
- Cryptography can be easy, do you know what ROT13 is? `cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_Ncualgvd}`

# Hints
- This can be solved online if you don't want to do it by hand!

# solucion
``` bash 
(kali㉿kali)-[~]
└─$ echo "cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_Ncualgvd}" | tr 'A-Za-z' 'N-ZA-Mn-za-m'  
picoCTF{next_time_I'll_try_2_rounds_of_rot13_Aphnytiq}

```
# bandera
- picoCTF{next_time_I'll_try_2_rounds_of_rot13_Aphnytiq}