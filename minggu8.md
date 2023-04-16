# Install Web Server di Linux

Berikut langkah - langkah untuk menginstall web server: 

1. pastikan dns server menggunakan dns server yang sudah  disediakan dan juga pastikan gateway sesuai dengan router
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/khhtbv7esjdalkki2odu.png)

2. Cek apakah jaringan sudah benar
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/7366xywsnbcr0gvyom63.png)
 
3. Kemudian dilanjutkan dengan menginstall **Nginx**, **MariaDB**, **Php**.
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/jp3y00iksuq1pc440ibo.png)

4. Setelah itu menginstall package utility yang digunakan untuk menginstall composer nantinya.
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ztuf3i66xyivxtq6bak4.png)

5. Download **composer.phar**, lalu pindah ke folder usr/bin agar bisa diakses sebagai program linux

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/tm2l9fkzwiij5uk5khv2.png)


![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ycqoezm00oj20es3uik5.png)

6. Cek hasilnya dengan melihat version dari **composer**
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/3hdg77l4xbyr4w5a70zl.png)

### Mencoba menginstall contoh projek laravel(php) dan dijalankan menggunakan Server

**Pertama**, clone dari github terlebih dahulu.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/p240y43qmk6i1vxcmw5f.png)
 
**Kedua** lakukan install package menggunakan composer

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/d2oi33urt57piry4wexf.png)

**Ketiga** Tambahkan konfigurasi project pada **Nginx**

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/fs5i0hquroi1ohhbjuo5.png)

**Terakhir** Setelah melakukan konfigurasi restart **service** nginx.


![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/rpg8yl9ft7n1vk032zoh.png)
