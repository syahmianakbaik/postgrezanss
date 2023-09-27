# Catatan command

Create database
``` psql
   CREATE DATABASE nama_database;
```

pindah ke database
``` psql
   \c nama_database;
```

hapus database
``` psql
    DROP DATABSE nama_database;
 ```
buat table
``` psql
    CRATE TABLE public.user(
    id SERIAL PRIMARY KEY 
    nama VARCHAR(100),
    saldo INT );
```