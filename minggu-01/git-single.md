
## INSTALASI GIT DI WINDOWS

1. Setelah download git , selanjutnya klik file yang telah didownload. Maka akan menampilkan seperti gambar ini , Klik next untuk lanjut

![img01](foto/01.png)

2. Selanjutnya pilih lokasi instal , akan tetapi lokasi instal akan ditampilkan secara langsung oleh karena itu biarkan saja dan klik Next

![img02](foto/02.png)

3. Selanjutnya pilih komponen , biarkan saja seperti itu dan klik next

![img03](foto/03.png)

4. Selanjutnya bagian menu select Components anda biarkan saja default kemudian klik Next

![img04](foto/04.png)

5. Selanjutnya pengaturan PATH Enviroment . Pilih yang tengah agar perintah git dapat dikenali di command 

![img05](foto/05.png)

6. Selanjutnya konversi line ending . Biarkan saja seperti ini , lanjut klik Next

![img06](foto/06.png)

7. Selanjutnya pilihlah emulator terminal. Pilih bagian kedua , lanjut klik next

![img07](foto/07.png)

8. Selanjutnya pilihlah opsi ekstra. Klik next untuk lanjut

![img08](foto/08.png)

9. Selanjutnya klik instal untuk memulai proses peninstalan

![img09](foto/09.png)

10. Tunggu proses install selesai

![img10](foto/10.png)

11. Setelah instal selesai klik finish

![img11](foto/11.png)

12. Seleasi maka anda dapat menggunakan git . Untuk menjalankan klik start menu , ketik "Git" selanjutnya akan ditampilkan pilihan "Git Bash" atau "Got GUI"

![img12](foto/12.png)

13. Tampilan jika anda menggunakan " Git Bash"

![img13](foto/13.png)

14. Tampilan jika anda menggunakan "Git GUI"

![img15](foto/15.png)


15. Untuk menggunakan CMD selanjutnya masukan perintah "git --version" untuk melihat apakah sudah terinstal atau belum jika sudah tampilan seperti ini

![img14](foto/14.png)

## Konfigurasi Git

Pada konfigurasi git dapat anda gunakan perintah git config. Salah satu hal pertama yang harus dilakukan adalah menyiapkan nama dan alamat email anda

![imgkon](foto/kon1.png)

Dari hasil konfigurasi git akan menampilkan hasil ini

![imgkon](foto/kon2.png)

![imgkon](foto/kon3.png)

Pada konfigurasi git hanya dilakukan satu kali saja, tetapi jika ingin dilulakan kembali jika melakukan perubahan nama dan email

### Mengelola Repo Sendiri di Account Sendiri

Dalam melakukan Repo anda harus suda mempunyai akun di Github .Selanjutnya langkah - langkahnya sebagai berikut :

# Membuat repo
Untuk membuat repo gunakan langkah berikut

1. Pertama klik tanda + pada bagian atas kanan setelah itu pilih New repository

![imgrep](foto/rep1.png)

2. Selanjutnya isikan nama repo,keterangan, serta lisensi sesui keinginan anda

![imgrep](foto/r1.png)

3. Selanjutnya klik Create repository

Setelah selesai repo akan dibuat dan dapat diakses. 

## Clon Repo

![imgclon](foto/r2.png)

# Mengelola Repo 
Setelah clone ke komputer local, semua manipulasi konten dilakukan di komputer lokal dan hasilnya akan dipush ke remote repo di Github. Maka dari itu jangan berganti - ganti remote local sekali dibuat disitu tetap disitu. Jika kehilangan repo lokal, clone ulang ke diktori yang bersih dan kosong setelah itu baru melakukan pengelolaan repo. Selanjutnya berikut hal yang dapat dilakukan.

# Mengubah Isi-Push Tanpa Bracnhing dan Mergin

Perubahan isi bisa terjadi karena satu atau kombinasi beberapa hal berikut:
  1. File dihapus
  2. File diedit
  3. Membuat file / direktori baru
  4. Menghapus direktori

Berikut melakukan perubahan di komputer lokal , setelah itu push ke repo
![imgclon](foto/r3.png)

Cara ini lebih mudah tetapi mempunyai resiko jika terjadi kesalahan dalam edit. Cara yang lebih aman tetapi memerlukan langkah yang lebih panjang adalah branching and merging

## Mengubah Isi dengan Branching and Merging

Pada bagian ini setiap kali melakukan perubahan di lokal komputer dengan membuat suatu cabang yang nantinya digunakan untuk menampung perubahan - perubahan. Setelah itu cabang akan di kirim ke repo Github untuk dimintai riview kemudian digabungkan (``` merge ```) ke main. Secara umum repo yang dibuat sudah akan mempunyai satu branc yang disebut ``` main ``` atau ``` master ```.

Berikut langkah - langkahnya sebagai berikut
1. Buat branch untuk menampung perubahan-perubahan
2. Lakukan perubahan-perubahan
3. Add dan commit perubahan-perubahan tersebut ke branch
4. Kembali ke repo master
5. Buat pull request di GitHub
6. Merge pull request di GitHub
7. Merge branch untuk menampung perubahan-perubahan tersebut ke master.
8. Selesai.

![imgclon](foto/r5.png)

Selanjutnya kirim pull request (*PR*)

![imgclon](foto/r6.png)

Setelah membuat PR , PR bisa di merge:

![imgclon](foto/r7.png)

Selanjutnya ``` Confirm Merge ```, branch yang kita kirimkan tadi sudah dimasukkan ke branch main. Setelah itu, merge di komputer lokal:

![imgclon](foto/r8.png)

# Sinkronisasi

Suatu saat, bisa saja terjadi kita menggunakan komputer lain dan mengedit repo melalui repo lokal di komputer lain, setelah itu pindah ke kamputer lain lagi. Saat itu, kita perlu melakukan sinkronisasi ke kemputer lokal. Perintah untuk sinkronisasi adalah:

$ git pull

Perintah ini dikerjakan di direktori tempat repo lokal kita berada.

# Membatalkan Perubahan
Praktik yang baik adalah membuat branch pada saat kita akan melakukan perubahan-perubahan. Jika perubahan-perubahan yang kita lakukan sudah sedemikian kacaunya, maka kita bisa membuat supaya perubahan-perubahan yang kacau tersebut hilang dan kembali ke kondisi bersih seperti semula.

![imgclon](foto/r9.png)

# Undo Commit Terakhir
Suatu saat, mungkin kita sudah terlanjur mem-push perubahan ke repo GitHub, setelah itu kita baru menyadari bahwa perubahan tersebut salah. Untuk itu, kita bisa melakukan git revert.

![imgclon](foto/r10.png)
![imgclon](foto/r11.png)

Contoh di atas adalah contoh untuk mengubah README.md dengan beberapa commit. Setelh itu, kita akan mengembalikan ke posisi terakhir sebelum commit terakhir.

Perintah di atas akan membuka editor. Pada editor tersebut kita bisa mengetikkan pesan revert ( = pesan commit untuk pembatalan). Setelah selesai, simpan:

![imgclon](foto/r12.png)

Selanjutnya, tinggal di-push ke repo GitHub.

![imgclon](foto/r13.png)

Jika commit sudah dilakukan, tetapi belum di-push ke repo GitHub (masih berada di lokal), cara membatalkannya:

![imgclon](foto/r14.png)

![imgclon](foto/r15.png)

Untuk kembali ke perubahan pada saat yang sudah lama, yang perlu dilakukan adalah melakukan git revert <posisi> kemudian mengedit secara manual kemudian push ke repo.

![imgclon](foto/r16.png)

Setelah itu, jika dilihat pada file, akan muncul tambahan untuk memudahkan meng-edit. File ini harus di-resolve terlebih dahulu, setelah itu baru di add dan commit:

![imgclon](foto/r17.png)

Edit file tersebut, setelah itu simpan

![imgclon](foto/r18.png)
  
Setelah itu, lanjutkan proses revert. Saat git revert --continue isikan pesan revert.

![imgclon](foto/r19.png)

















