### 1. Kernel 

Kernel adalah core/inti dari sistem komputer. Kernel merupakan bagian dari OS dengan kata lain kernel adalah perangkat lunak yang membantu program program komputer untuk memanfaatkan resource/hardware yang ada di komputer.Pada umumnya pasti ada scheduler, supervisor, interrupt handler, dan memory manager.

Scheduler berfungsi untuk mengatur pembagian waktu dan urutan dari proses-proses yang ingin mendapatkan servis dari kernel. Supervisor berfungsi untuk memberikan servis oleh kernel kepada proses yang sudah dijadwalkan. Interrupt handler berfungsi untuk menangani seluruh permintaan dari hardware yang ingin mendapatkan servis dari kernel. Memori manager berfungsi untuk mengatur alokasi alamat di memori.

#### Jenis - jenis kernel

Ada 4 jenis kernel dan ke empat - empatnya memiliki perbedaan masing masing:
a. Monolithic
Seluruh fungsi dasar dari sistem operasi berada di kernel itu sendiri. Sehingga membuat penggunaan kernel menjadi lebih efisien namun lebih berkemungkinan besar untuk mendapatkan crash dengan kata lain jenis ini kurang stable.

b. Mikrokernel
Hanya mencakup fungsi minimal dari sistem operasi, manajemen pengalamatan memori, manajemen proses/thread, dan inter-process communication.  Kelebihan microkernel adalah stabilitas sistem lebih terjaga dan kekurangannya adalah komunikasi antara proses menjadi lebih rumit sehingga sistem menjadi tidak efisien.

c. Hybrid Kernel
Mirip dengan mikrokernel hanya saja di Hybrid kernel ditambah dengan kode sehingga penggunaannya menjadi lebih efisien.

d. Exokernel
Masih merupakan disain eksperimental dan dalam tahap penelitian sehingga belum dipakai secara luas. Perbedaan konsep disain exokernel dengan disain kernel lainnya adalah exokernel memiliki fungsi perlindungan dan pembagian resource untuk hardware. Kelebihan exokernel adalah bisa dimasukkan library sistem operasi lebih dari satu sehingga bisa menjalankan program-program untuk sistem operasi yang berbeda secara bersamaan.

### 2.  Direktori di linux
(root) : merupakan induk dari susunan direktori di linux dan merupakan tempat dimana semua direktori berada.

/bin/ : directory ini berisi progam perintah esensial yang dibutuhkan oleh semua user. progam-progam disini dapat dijalankan, meskipun tidak ada sistem file lain yang di mount. Directory ini tidak memiliki subdirectory.

/boot/ : merupakan direktori yang berfungsi untuk menyimpan konfigurasi dan file-file yang berhubungan dengan proses booting, memuat Linux Kernel dan file lain yang diperlukan LILO dan GRUB boot manager.

/dev/ : merupakan direktori yang berfungsi untuk menyimpan konfigurasi device atau hardware dari sistem, seperti harddisk (hda, sda), terminal (tty) etc.

/etc/ : merupakan direktori yang berfungsi untuk menyimpan skrip installation pada /etc/rc.d subdirektory dan file-file konfigurasi dari sistem, misalkan konfigurasi service, penjadwalan etc.

/home/: berfungsi untuk menyimpan data/dokumen untuk user yang ada di komputer linux.

/root/ (root directory) : adalah struktur paling dasar yang harus bisa melakukan boot, perbaikan atau mengembalikan sistem seperti dalam keadaan semula.

/lib/ : merupakan direktori yang berfungsi untuk menyimpan library dasar dari system termasuk modul driver yang dapat diisi pada sistem boot.

/media/ : direktori yang berfungsi untuk mounting removable media seperi drive CD-ROM, floopy disk etc.

/opt/ : merupakan direktori yang berfungsi untuk menyimpan aplikasi tambahan diluar aplikasi bawaan dari linux.

/sbin/ : merupakan direktori yang berfungsi untuk menyimpan aplikasi dasar dari linux yang dijalankan oleh super user (root) misalnya mount, shutdown, umount.

/usr/ : merupakan direktori untuk menyimpan aplikasi yang diinstall oleh user, misalkan OpenOffice, Kate , chrome dan sebagainya.

/var/ : merupakan direktori untuk menyimpan informasi pencatatan log sistem, web server, mailbox dan data-data aplikasi.

/tmp/ : berisi file-file sementara yang dibutuhkan sebuah aplikasi yang sedang berjalan.

/mnt/ : yang berisikan mount point tempat untuk kamu memasang floopy-disk dan CD-ROM.

/srv/ : direktori yang berisikan data atau service yang dibutuhkan oleh sebuah server misalnya,menjalankan FTP server.

### 3. Perbedaan sudo dan su

Perbedaanya terletak di kenapa digunakan. **SU** digunakan untuk switch user digunakan untuk mengubah user di linux, jika tidak di set maka akan di set root.User root memliki password yang berbeda dengan user biasa. Pada user root, bisa mengkases semua yang ada dilinux, Sedangkan **SUDO **digunakan untuk menggunakan perintah yang membutuhkan akses sebagai _root_, artinya perintah itu bisa digunakan oleh user biasa namun harus memasukan password dimana password yang dimasukan berbeda dengan password yang sudah di user _root_.

### 4. Repository di Linux

Repository Linux adalah lokasi penyimpanan tempat sistem Anda mengambil dan menginstal pembaruan dan aplikasi OS. Setiap repository adalah kumpulan perangkat lunak yang di-host di server jauh dan dimaksudkan untuk digunakan untuk menginstal dan memperbarui paket perangkat lunak pada sistem Linux.

Jadi pada saat menjalankan ```apt update```, perintah tersebut akan mengupdate versi dari repository yang ada di linux. Untuk list dari repository ada di folder **etc/source.list** kemudian selain itu jika diperlukan maka akan ditambahkan repository lagi jika package yang diinginkan tidak ada di repository lokal. Ada beberapa jenis repository lokal:

- Main – perangkat lunak sumber terbuka yang didukung secara resmi. Canonical memberikan dukungan resmi untuk paket-paket ini. Setiap paket perangkat lunak sumber terbuka yang disertakan dalam instalasi default disertakan bersama dengan beberapa paket penting lainnya.
- Restricted – yang didukung secara resmi, perangkat lunak sumber tertutup – mis., Driver perangkat keras – didukung selama rilis.
- Universe – dikelola komunitas, sumber terbuka. Mayoritas perangkat lunak Ubuntu berasal dari repositori ini. Canonical tidak memberikan dukungan atau pembaruan resmi.
- Multiverse – perangkat lunak yang tidak didukung, sumber tertutup, dan terbebani paten.

### 5. Perintah APT

Dalam linux digunakan untuk menginstal, memperbarui, menghapus dan mengelola paket di distro linux yang berbasis debian. Perintah ini harus digunakan dengan menggunakan sudo karena memerlukan hak akses khusus. Ada beberapa yang bisa dilakukan apt

##### - Mengupdate indeks package

Ini digunakan dengan melakukan perintah ```sudo apt update```, yang mana fungsinya indeks paket yang berada dilinux. Pada dasarnya linux menyimpan indeks package di semacam database dimana untuk mengupdate harus di update indeksnya

##### - Mengupgrade indeks package

Perintah ini dilakukan untuk mengupgarde versi package menjadi yang terbaru. Cara penulisannya dengan ```sudo apt upgrade```, jika tidak dispesifikan package nya maka akan menupgrade banyak/semua package yang ready untuk diupgrade. Contoh yang menspesifikan package ```sudo apt upgrade firefox```.

##### - Menginstall package 

Salah satu perintah penting lainnya adalah menginstall package dengan ```sudo apt install <nama package>``` maka akan mendownload package dari repository. Bisa juga langsung menggunakan file .deb caranya ```sudo apt install /file/package.deb```.

##### - Menghapus package

Untuk menguninstal paket dengan menggunakan apt, gunakan perintah berikut :

```sudo apt remove package_name``` Kita juga dapat menentukan beberapa paket untuk di uninstall. Perintah **remove** akan menghapus instalasi paket yang diberikan tetapi mungkin meninggalkan beberapa file konfigurasi. Jika Anda ingin menghapus paket termasuk semua file konfigurasi gunakan perintah purge alih-alih remove ```sudo apt purge package_name```


