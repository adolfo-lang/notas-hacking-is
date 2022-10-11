## insp3ctor

# objetivo
- Kishor Balan tipped us off that the following code may need inspection: `https://jupiter.challenges.picoctf.org/problem/9670/` ([link](https://jupiter.challenges.picoctf.org/problem/9670/)) or http://jupiter.challenges.picoctf.org:9670

# Hints
- How do you inspect web code on a browser?
- There's 3 parts

# solucion
``` bash 
inspeccionamos el html, javascript y el css, ahí encontramos las partes
de la bandera.
</p>
	<!-- Html is neat. Anyways have 1/3 of the flag: picoCTF{tru3_d3 -->
      </div>
/* You need CSS to make pretty pages. Here's part 2/3 of the flag: t3ct1ve_0r_ju5t */
/* Javascript sure is neat. Anyways part 3/3 of the flag: _lucky?2e7b23e3} */
```
# bandera
- picoCTF{tru3_d3t3ct1ve_0r_ju5t2e7b23e3}