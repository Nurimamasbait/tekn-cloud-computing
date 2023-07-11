# Application Containerization and Microservice Orchestration

Pada pertemuan ini mempelajari tentang containerization aplikasi dasar menggunakan Docker dan menjalankan berbagai komponen aplikasi sebagai layanan mikro. Pada praktik kali ini mengguanakan Docker Compose untuk orkestrasi selama pengembangan
## Stage Setup
Pada tahap pertama mengkloning repositori kode demo mengubah direktori kerja, dan memeriksa cabangnya.demo

![img](foto11/1.png)

## Basic Link Extractor Script
Dalam tahap ini memeriksa cabang dan daftar file didalam step0

![img](foto11/2.png)

berikut ini melihat isi dari file linkextractor.py

![img](foto11/3.png)

dari hasil di atas merupakan scrip Python yang mengimpor tiga paket yaitu from the standard library and two popular third-party packages and. 
Dari file diatas ternyata  merupakan file yang tidak memenuhi persyaratannya ntuk dijalankan pada mesin
Berikut merupakan file yang menyarankan cara menjalankan

![img](foto11/4.png)

pada file diatas terdapat kesalahan dengan itu perlu memeriksa izin pada file ini:Permission denied. Untuk pemeriksaan dapat menjalankan perintah berikut

![img](foto11/5.png)

dari hasil menjalankan perintah di atas menunjukan bahwa skrip tidak diatur untuk dapat dieksekusi. Oleh sebab itu dapat mengubahnya dengan menjalankan atau menjalankannya sebagai program Python alih-alih skrip yang dijalankan sendiri seperti yang di hasilkan seperti diatas

Pada tahap di atas tersebut mendapat pesan pertama yaitu kehilangan paket pihak ketiga yang dibutuhkan oleh skrip. Dengan itu dapat menginstal paket Python  (dan berpotensi paket lain yang hilang) menggunakan salah satu dari banyak teknik untuk membuatnya bekerja, tetapi terlalu banyak pekerjaan untuk skrip sederhana seperti itu, memungkinkan tidak jelas bagi mereka yang tidak terbiasa dengan ekosistem Python.

## Containerized Link Extractor Script
Dalam tahap ini memeriksa cabang dan daftar file didalam step1

![img](foto11/6.png)

Berikut menambahkan satu file baru

![img](foto11/7.png)

Dari tahap diatas dapat menyiapkan Docker image untuk skrip.

Berikut menggambarkan Docker image tetapi tidak benar-benar membangunnya

![img](foto11/8.png)

![img](foto11/9.png)

![img](foto11/10.png)

![img](foto11/11.png)

![img](foto11/12.png)

## Link Extractor Module with Full URI and Anchor Text
Dalam tahap ini memeriksa cabang dan daftar file didalam step2

![img](foto11/13.png)


Dalam langkah ini skrip diperbarui dengan perubahan fungsional berikut:linkextractor.py

1. Jalur dinormalisasi ke URL lengkap
2. Melaporkan tautan dan teks jangkar
3. Dapat digunakan sebagai modul dalam skrip lain

Berikut  melihat scrip yang telah diperbarui 

![img](foto11/14.png)

Berikut membuat image baru dan melihat perubahan
![img](foto11/15.png)

![img](foto11/16.png)

![img](foto11/17.png)

![img](foto11/18.png)

## Link Extractor API Service

![img](foto11/19.png)

Perubahan berikut telah dibuat dalam langkah ini:

1. Menambahkan skrip server yang menggunakan modul ekstraksi tautan yang ditulis pada langkah terakhirmain.py
2. Diperbarui untuk merujuk ke file sebagai gantinyaDockerfilemain.py
3. Server dapat diakses sebagai WEB API di http://<hostname>[:<prt>]/api/<url>
4. Dependensi dipindahkan ke filerequirements.txt
5. Perlu pemetaan port untuk membuat layanan dapat diakses di luar kontainer (server yang digunakan di sini mendengarkan port secara default)Flask5000

Berikut melihat perubahannya:Dockerfile

![img](foto11/20.png)

![img](foto11/21.png)

![img](foto11/22.png)

![img](foto11/23.png)

![img](foto11/24.png)

![img](foto11/25.png)

![img](foto11/26.png)

![img](foto11/27.png)

## Link Extractor API and Web Front End Services

![img](foto11/28.png)

![img](foto11/29.png)

![img](foto11/30.png)

![img](foto11/31.png)

![img](foto11/32.png)

Berikut mengakses web http://example.com/ ,Dengan itu menjalankan perintah berikut untuk dapat mengakses link 
![img](foto11/33.png)

setelah perintah dijalankan http://example.com/ , maka akan menampilkan seperti dibawah ini

![img](foto11/a.png)

kemudian isi dengan autan berikut .https://training.play-with-docker.com/

![img](foto11/c.png)

![img](foto11/34.png)

![img](foto11/35.png)

![img](foto11/36.png)

![img](foto11/37.png)

![img](foto11/38.png)


![img](foto11/39.png)

![img](foto11/40.png)

![img](foto11/41.png)

![img](foto11/42.png)

![img](foto11/43.png)

![img](foto11/44.png)

![img](foto11/45.png)

![img](foto11/46.png)

![img](foto11/47.png)

![img](foto11/48.png)

![img](foto11/49.png)

![img](foto11/50.png)

![img](foto11/51.png)

![img](foto11/52.png)

![img](foto11/53.png)

![img](foto11/54.png)

![img](foto11/55.png)
