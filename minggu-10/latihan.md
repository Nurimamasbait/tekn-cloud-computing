# PERTEMUAN 10
 # Dasar-dasar Jaringan
Perintah Jaringan Docker
Perintah adalah perintah utama untuk mengkonfigurasi dan mengelola jaringan kontainer. Jalankan perintah dari terminal pertama.docker networkdocker network

![img](foto/1.png)

Daftar jaringan
Jalankan perintah untuk melihat jaringan kontainer yang ada di host Docker saat ini.docker network ls

![img](foto/2.png)

Periksa jaringan
Perintah ini digunakan untuk melihat detail konfigurasi jaringan

![img](foto/3.png)

Daftar plugin driver jaringanV
Perintah menunjukkan banyak informasi menarik tentang instalasi Docke

![img](foto/4.png)

Jaringan Jembatan
Dasar-dasar
Setiap instalasi Docker yang bersih dilengkapi dengan jaringan pra-bangun yang disebut bridge. Verifikasi ini dengan ekstensi .docker network lsV

![img](foto/5.png)

Output di atas menunjukkan bahwa jaringan bridge dikaitkan dengan driver bridge dan juga menunjukkan bahwa jaringan jembatan dicakup secara lokal. Ini berarti bahwa jaringan hanya ada di host Docker ini. Ini berlaku untuk semua jaringan yang menggunakan driver bridge - driver bridge menyediakan jaringan host tunggal.

Instal perintah dan gunakan untuk membuat daftar jembatan Linux di host Docker Anda. Anda dapat melakukan ini dengan menjalankan file .brctlsudo apt-get install bridge-utils

![img](foto/6.png)

Kemudian, daftarkan bridge di host Docker Anda, dengan menjalankan .brctl show
Output berikut menunjukkan satu jembatan Linux yang disebut docker0. Ini adalah jembatan yang secara otomatis dibuat untuk jaringan jembatan. Anda dapat melihat bahwa ia tidak memiliki antarmuka yang saat ini terhubung dengannya.

![img](foto/7.png)

perintah untuk melihat detail bridge docker0

![img](foto/8.png)

Menyambungkan kontainer
Jaringan bridge adalah jaringan default untuk kontainer baru. Ini berarti bahwa kecuali Anda menentukan jaringan yang berbeda, semua kontainer baru akan terhubung ke jaringan jembatan

![img](foto/9.png)

Perintah ini akan membuat kontainer baru berdasarkan gambar dan akan menjalankan perintah untuk menjaga kontainer tetap berjalan di latar belakang.

![img](foto/10.png)

Jalankan perintah lagi.brctl show
![img](foto/11.png)

melihat kontainer baru yang terpasang
![img](foto/12.png)

Uji konektivitas jaringan
Output ke perintah sebelumnya menunjukkan alamat IP kontainer baru

![img](foto/13.png)

Balasan di atas menunjukkan bahwa host Docker dapat melakukan ping ke kontainer melalui jaringan bridge. Tapi, kami juga dapat memverifikasi kontainer dapat terhubung ke dunia luar juga

![img](foto/14.png)
![img](foto/15.png)
![img](foto/16.png)
![img](foto/17.png)
![img](foto/18.png)
![img](foto/19.png)
![img](foto/20.png)
![img](foto/21.png)
![img](foto/22.png)
![img](foto/23.png)
![img](foto/24.png)
![img](foto/25.png)
![img](foto/26.png)
![img](foto/27.png)
![img](foto/28.png)
![img](foto/29.png)
![img](foto/30.png)
![img](foto/31.png)
![img](foto/32.png)
![img](foto/33.png)
![img](foto/34.png)
![img](foto/35.png)
![img](foto/36.png)
![img](foto/37.png)
![img](foto/38.png)
