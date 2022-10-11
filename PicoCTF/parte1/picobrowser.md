## picobrowser

# objetivo
- This website can be rendered only by **picobrowser**, go and catch the flag! `https://jupiter.challenges.picoctf.org/problem/28921/` ([link](https://jupiter.challenges.picoctf.org/problem/28921/)) or http://jupiter.challenges.picoctf.org:28921

# Hints
- You don't need to download a new web browser

# solucion
``` bash 

en este reto al pedir la bandera el navegador se da cuenta
que no somos pico browser, por lo cual debemos cambiar el user-agent
(kali㉿kali)-[~]
└─$ curl -s https://jupiter.challenges.picoctf.org/problem/28921/flag -H "User-Agent: picobrowser" | grep picoCTF     
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{p1c0_s3cr3t_ag3nt_84f9c865}</code></p>
```

# bandera
- picoCTF{p1c0_s3cr3t_ag3nt_84f9c865}