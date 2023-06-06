# INSTALL DOCKER
1. Download Docker untuk windows

![img](foto7/1.png)

2. Mulai install docker

![img](foto7/2.png)

3. konfigurasi 

![img](foto7/3.png)

4. Proses install

![img](foto7/4.png)

5. Instalasi selesai
Setelah itu , klik Close and restrart untuk restart komputer
![img](foto7/5.png)

# 2. Get Started - Docker
##  Containerize an application
Gunakan app
Kloning repositori memulai menggunakan perintah berikut:

![img](foto7/d1.png)

Lihat konten repositori kloning. Di dalam direktori Anda harus melihat dan dua subdirektori  dan.(getting-started/apppackage.jsonsrcspec)

![img](foto7/d2.png)

## Membuat gambar kontainer aplikasi

Di direktori, lokasi yang sama dengan file, buat file bernama . Anda dapat menggunakan perintah berikut di bawah ini untuk membuat Dockerfile berdasarkan sistem operasi Anda.apppackage.jsonDockerfile

![img](foto7/d3.png)

Buat gambar kontainer

![img](foto7/d4.png)

Login Docker

![img](foto7/d5.png)

Mulai kontainer Anda menggunakan perintah dan tentukan nama gambar yang baru saja Anda buat:docker run

![img](foto7/d6.png)


Setelah beberapa detik, buka browser web Anda untuk http://localhost:3000. Anda akan melihat aplikasi Anda.

![img](foto7/d7.png)

Jalankan perintah berikut di terminal untuk mencantumkan kontainer Anda.docker ps
Dan hasilnya sebagai berikut

![img](foto7/d8.png)



