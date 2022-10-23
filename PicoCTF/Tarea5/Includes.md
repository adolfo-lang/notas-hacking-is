## Includes

# objetivo
- Can you get the flag? Go to this [website](http://saturn.picoctf.net:54634/) and see what you can discover.

# Hints
- Is there more code than what the inspector initially shows?

# solucion
``` bash 
inspeccionamos el codigo y la bandera la encontramos en los archivos .css
y .js
body {
  background-color: lightblue;
}

/*  picoCTF{1nclu51v17y_1of2_  */
function greetings()
{
  alert("This code is in a separate file!");
}

//  f7w_2of2_df589022}

```
# bandera
- picoCTF{1nclu51v17y_1of2_f7w_2of2_df589022}