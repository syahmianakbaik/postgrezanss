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

untuk membuat  table provider
```psql
 ALTER TABLE public.provider ADD CONSTRAINT fk_user FOREIGN KEY (user_id) REFERENCES public.user(id);
```

untuk menambahkan provider
```psql
INSERT INTO provider (user_id, nama) VALUES (2, 'TELKOMSEL');
```

untuk menyatukan antar 2 table 
```psql
 SELECT a.*, b.nama as kartu FROM public.user as a LEFT JOIN public.provider as b on b.user_id=2;
```

untuk lebih memperjelas seorang user 
```psql
 WHERE a.id=2;
```