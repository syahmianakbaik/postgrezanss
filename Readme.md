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

untuk menampilkan semua data
```psql
     SELECT * FROM public.user;
```

untuk membuat sebuah data user
```psql
 INSERT INTO public.USER (nama, saldo) VALUES ('fauzan syah', 0);
```

untuk mengupdate sebuah data user
```psql
 UPDATE public.user SET saldo=10000000 WHERE id=1;
```

untuk menghapus sebuah data user
```psql
 DELETE FROM public.user WHERE id=1;
```

untuk membuat  penghubung antar table
```psql
 ALTER TABLE public.provider ADD CONSTRAINT fk_user FOREIGN KEY (user_id) REFERENCES public.user(id);
```