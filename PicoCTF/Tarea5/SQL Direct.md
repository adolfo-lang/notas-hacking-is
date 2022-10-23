## SQL Direct

# objetivo
- Connect to this PostgreSQL server and find the flag!

# Hints
- What does a SQL database contain?

# solucion
``` bash 
nos conectamos a la base de datos de pico y buscamos la bandera
(kali㉿kali)-[~]
└─$ psql -h saturn.picoctf.net -p 49651 -U postgres pico
Password for user postgres: 
psql (14.5 (Debian 14.5-1), server 14.2 (Debian 14.2-1.pgdg110+1))
Type "help" for help.

pico=# \l
                                 List of databases
   Name    |  Owner   | Encoding |  Collate   |   Ctype    |   Access privileges   
-----------+----------+----------+------------+------------+-----------------------
 pico      | postgres | UTF8     | en_US.utf8 | en_US.utf8 | 
 postgres  | postgres | UTF8     | en_US.utf8 | en_US.utf8 | 
 template0 | postgres | UTF8     | en_US.utf8 | en_US.utf8 | =c/postgres          +
           |          |          |            |            | postgres=CTc/postgres
 template1 | postgres | UTF8     | en_US.utf8 | en_US.utf8 | =c/postgres          +
           |          |          |            |            | postgres=CTc/postgres
(4 rows)
pico=# \dt
         List of relations
 Schema | Name  | Type  |  Owner   
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)

pico=# select * from flags;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)

```
# bandera
- picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}