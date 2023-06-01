# 1.INSTAL GO, MYSQL DAN MONGODB  
### Instal Go
1. Buka file go yang telah didownload, kemudian klik dan klik run

![img](foto6/2.1.png)

2. selanjutnya klik next

![img](foto6/22.png)

3. klik next

![img](foto6/23.png)

4. Selanjutnya memilih folder yang ingin anda letakan file Go yang akan diinstal

![img](foto6/24.png)

5. Selanjutnya klik Install

![img](foto6/25.png)

6. Kemudian tunggu sampai proses install selesai

![img](foto6/26.png)

7. Dan setelah selesai klik Finish

![img](foto6/27.png)

8. Setelah terinstal , buka cmd untuk melihat apakah Go sudah terinstal

![img](foto6/go.png)

### Install MYSQL

Jika anda telah install mysql anda dapat melihat perintah untuk melihat version mysql

![img](foto6/01.png)

### Install MongoDB
1. Klik file MongoDB yang telah didownload

![img](foto6/3.png)

2. Selanjutnya klik next

![img](foto6/4.png)

3. Lanjut Next

![img](foto6/5.png)

4. Selanjutnya akan menampilkan Servir Configuration
Pada bagian ini akan di perlihatkan lokasi datanya , bias dilihat pada tanda

![img](foto6/6.png)

5. Hilangkan tanda Install MongoDB Compass dan klik nxt

![img](foto6/7.png)

6. Selanjutnya klik Install

![img](foto6/8.png)

7. Kemudian tunggu proses install selesai

![img](foto6/9.png)

8. Setelah installan selesai maka Finish , setelah itu klik finish

![img](foto6/10.png)

9. Selanjutnya buka Folder MongoDB, kemudian klik mongoDB.exe

![img](foto6/11.png)

10. Maka tampilan mongoDB jika telah seperti di bawah ini maka telah berasil terinstall

![img](foto6/12.png)

# 2. Contoh Program Go masing-masing untuk koneksi dan membaca data dari MySQL dan MongoDB

#### 1. Program Go koneksi MYSQL

Pertama-tama, Kita perlu men-download driver menggunakan go get.

![img](foto6/1sa.png)

Buat file main.go

![img](foto6/2s.png)

Selanjutnya run file main.go dan hasil sukses maka koneksi ke mysql berhasil

![img](foto6/s3.png)

Selanjutnya membuat database

![img](foto6/s4.png)

![img](foto6/s5.png)

Membuat file dengan nama select.go untuk menghubungkan database yang telah dibuat

![img](foto6/s6.png)

Selanjutnya run file select.go

![img](foto6/s7.png)

#### 2. Program Go koneksi MongoDB

Pertama-tama, Kita perlu men-download driver menggunakan go get.

![img](foto6/ba1.png)

Membuat file mongodb.go

![img](foto6/b3.png)

Selanjutnya run file mongodb.go

![img](foto6/ba2.png)

# 3. Dengan menggunakan Gin, buatlah RESTful API untuk membaca dara dari MySQL dan MongoDB tersebut

1. Program Main.go

![img](foto6/gin1.png)

2. Run main untuk akses GIN

![img](foto6/gin2.png)

3. Hasil

![img](foto6/gin3.png)





