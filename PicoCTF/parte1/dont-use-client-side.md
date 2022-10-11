## dont-use-client-side

# objetivo
- Can you break into this super secure portal? `https://jupiter.challenges.picoctf.org/problem/17682/` ([link](https://jupiter.challenges.picoctf.org/problem/17682/)) or http://jupiter.challenges.picoctf.org:17682

# Hints
- Never trust the client

# solucion
``` bash 
la contraseña esta oculta en el html, ya que en el java script
lo esta validando en pequeñas partes, ya que la bandera esta descompuesta ahi mismo, para encontrarla hay que seguir la logica para armar la bandera.
if (checkpass.substring(0, split) == 'pico') {
      if (checkpass.substring(split*6, split*7) == '706c') {
        if (checkpass.substring(split, split*2) == 'CTF{') {
         if (checkpass.substring(split*4, split*5) == 'ts_p') {
          if (checkpass.substring(split*3, split*4) == 'lien') {
            if (checkpass.substring(split*5, split*6) == 'lz_b') {
              if (checkpass.substring(split*2, split*3) == 'no_c') {
                if (checkpass.substring(split*7, split*8) == '5}') {
                  alert("Password Verified")
```
# bandera
- picoCTF{no_clients_plz_b706c5}