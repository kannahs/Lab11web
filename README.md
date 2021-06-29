# Praktikum 11 & 13: PHP Framework (Codeigniter)
## Langkah-Langkah
- Aktifkan ekstensi pada xampp dengan cara, buka xampp pada bagian apache klik config dan buka php.ini

![a0](https://github.com/kannahs/Lab11web/blob/master/Image/a0.PNG?raw=true)

- Untuk mengaktifkan nya hapus tanda (;) .
![a01](https://github.com/kannahs/Lab11web/blob/master/Image/a01.PNG?raw=true)

- Unduh Codeigniter dari website https://codeigniter.com/download
- Extrak file zip Codeigniter ke direktori htdocs/lab11_ci.
- Ubah nama direktory framework-4.x.xx menjadi ci4.

![a1](https://github.com/kannahs/Lab11web/blob/master/Image/a1.PNG?raw=true)

- Buka browser dengan alamat http://localhost/lab11_ci/ci4/public/

![a2](https://github.com/kannahs/Lab11web/blob/master/Image/a2.PNG?raw=true)

- Codeigniter 4 menyediakan CLI untuk mempermudah proses development.Untuk mengakses CLI buka terminal/command prompt.
- Arahkan lokasi direktori sesuai dengan direktori kerja project dibuat (xampp/htdocs/lab11_ci/ci4/)
- Perintah yang dapat dijalankan untuk memanggil CLI Codeigniter adalah php spark:

![a3](https://github.com/kannahs/Lab11web/blob/master/Image/a3.PNG?raw=true)

![a3-1](https://github.com/kannahs/Lab11web/blob/master/Image/a3-1.PNG?raw=true)

- Codeigniter 4 menyediakan fitur debugging untuk memudahkan developer untuk mengetahui pesan error apabila terjadi kesalahan dalam membuat kode program. Secara default fitur ini belum aktif. Ketika terjadi error pada aplikasi akan ditampilkan pesan kesalahan seperti berikut.

![a4](https://github.com/kannahs/Lab11web/blob/master/Image/a4.PNG?raw=true)

- Semua jenis error akan ditampilkan sama. Untuk memudahkan mengetahui jenis errornya, maka perlu diaktifkan mode debugging dengan mengubah nilai konfigurasi pada environment variable CI_ENVIRONMENT menjadi development.
- Ubah nama file env menjadi .env kemudian buka file tersebut dan ubah nilai variable CI_ENVIRONMENT menjadi development.

![a5](https://github.com/kannahs/Lab11web/blob/master/Image/a5.PNG?raw=true)

- Ini hasil errornya .

![a6](https://github.com/kannahs/Lab11web/blob/master/Image/a6.PNG?raw=true)

- Contoh error yang terjadi. Untuk mencoba error tersebut, ubah kode pada file app/Controller/Home.php hilangkan titik koma pada akhir kode.
- Membuat route baru dengan menambah kan kode yang ada pada line 35-38.

![a7](https://github.com/kannahs/Lab11web/blob/master/Image/a7.PNG?raw=true)

- Untuk mengetahui route yang ditambahkan sudah benar, buka CLI dan jalankan perintah berikut (php spark routes).

![a8](https://github.com/kannahs/Lab11web/blob/master/Image/a8.PNG?raw=true)

- Selanjutnya coba akses route yang telah dibuat dengan mengakses alamat url http://localhost:8080/about
![a9](https://github.com/kannahs/Lab11web/blob/master/Image/a9.PNG?raw=true)

- karena file/page tersebut tidak ada buat dulu controller yang sesuai yaitu controller page
- Buat file baru dengan nama page.php pada direktori Controller kemudian isi kodenya seperti berikut.
![a10](https://github.com/kannahs/Lab11web/blob/master/Image/a10.PNG?raw=true)

- hasilnya.

![a11](https://github.com/kannahs/Lab11web/blob/master/Image/a11.PNG?raw=true)

- Tambahkan method baru pada Controller Page seperti berikut (function tos).
![a12](https://github.com/kannahs/Lab11web/blob/master/Image/a12.PNG?raw=true)

- Method ini belum ada pada routing, sehingga cara mengaksesnya dengan menggunakan alamat: http://localhost:8080/page/tos hasilnya. 

![a13](https://github.com/kannahs/Lab11web/blob/master/Image/a13.PNG?raw=true)

- Buat file baru dengan nama about.php pada direktori view (app/view/about.php)
![a14](https://github.com/kannahs/Lab11web/blob/master/Image/a14.PNG?raw=true)

- Ubah method about pada class Controller Page menjadi seperti berikut:
![a15](https://github.com/kannahs/Lab11web/blob/master/Image/a15.PNG?raw=true)

- hasilnya.
![a16](https://github.com/kannahs/Lab11web/blob/master/Image/a16.PNG?raw=true)

- Buat file css pada direktori public dengan nama style.css (copy file dari praktikum lab4_layout. Kita akan gunakan layout yang pernah dibuat pada praktikum 4.
- Kemudian buat folder template pada direktori view kemudian buat file header.php dan footer.php
![a17](https://github.com/kannahs/Lab11web/blob/master/Image/a17.PNG?raw=true)

![a18](https://github.com/kannahs/Lab11web/blob/master/Image/a18.PNG?raw=true)

![a19](https://github.com/kannahs/Lab11web/blob/master/Image/a19.PNG?raw=true)

- OUTPUTNYA .
![a20](https://github.com/kannahs/Lab11web/blob/master/Image/a20.PNG?raw=true)


## Tugas 
1 Lengkapi kode program untuk menu lainnya yang ada pada Controller Page, sehinggasemua link pada navigasi header dapat menampilkan tampilan dengan layout yang sama.

- Disini saya hanya menambahkan input untuk menampilkan contact,faqs, dan tos
![tugasA](https://github.com/kannahs/Lab11web/blob/master/Image/tugasA.PNG?raw=true)

- Hasil halaman contact

![tugasB](https://github.com/kannahs/Lab11web/blob/master/Image/tugasB.PNG?raw=true)

- Halaman FAQS .

![tugasB1](https://github.com/kannahs/Lab11web/blob/master/Image/tugasB1.PNG?raw=true)

- Halaman Term of services

![tugasB2](https://github.com/kannahs/Lab11web/blob/master/Image/tugasB2.PNG?raw=true)

# Praktikum 13

- Membuat tabel user.

![a1](https://github.com/kannahs/Lab11web/blob/master/Image%20praktikum%2013/a1.PNG?raw=true)

- Membuat model user
- Buat file baru pada direktori app/Models dengan nama UserModel.php.

![a2](https://github.com/kannahs/Lab11web/blob/master/Image%20praktikum%2013/a2.PNG?raw=true)

-Buat Controller baru dengan nama User.php pada direktori app/Controllers.Kemudian tambahkan method index() untuk menampilkan daftar user, dan method login() untuk proses login. 

![a3](https://github.com/kannahs/Lab11web/blob/master/Image%20praktikum%2013/a3.PNG?raw=true)

- Buat direktori baru dengan nama user pada direktori app/views, kemudian buat file baru dengan nama login.php.

![a4](https://github.com/kannahs/Lab11web/blob/master/Image%20praktikum%2013/a4.PNG?raw=true)

- Buka CLI, kemudian tulis perintah berikut:

![a5](https://github.com/kannahs/Lab11web/blob/master/Image%20praktikum%2013/a5.PNG?raw=true)

- Selanjutnya, buka file UserSeeder.php yang berada di lokasi direktori /app/Database/Seeds/UserSeeder.php kemudian isi dengan kode berikut:

![a6](https://github.com/kannahs/Lab11web/blob/master/Image%20praktikum%2013/a6.PNG?raw=true)

- Selanjutnya buka kembali CLI dan ketik perintah berikut:

![a7](https://github.com/kannahs/Lab11web/blob/master/Image%20praktikum%2013/a7.PNG?raw=true)

- Selanjutnya buka url http://localhost:8080/user/login seperti berikut: 

![b8](https://github.com/kannahs/Lab11web/blob/master/Image%20praktikum%2013/b8.PNG?raw=true)

- Selanjutnya membuat filer untuk halaman admin. Buat file baru dengan nama Auth.php pada direktori app/Filters.

![a9](https://github.com/kannahs/Lab11web/blob/master/Image%20praktikum%2013/a9.PNG?raw=true)

- Selanjutnya buka file app/Config/Filters.php tambahkan kode berikut:

![a10](https://github.com/kannahs/Lab11web/blob/master/Image%20praktikum%2013/a10.PNG?raw=true)

- Selanjutnya buka file app/Config/Routes.php dan sesuaikan kodenya.

![a11](https://github.com/kannahs/Lab11web/blob/master/Image%20praktikum%2013/a11.PNG?raw=true)

- Buka url dengan alamat http://localhost:8080/admin/artikel ketika alamat tersebut diakses maka, akan dimuculkan halaman login.

![b11](https://github.com/kannahs/Lab11web/blob/master/Image%20praktikum%2013/b11.PNG?raw=true)

- Tambahkan method logout pada Controller User seperti berikut:

![A12](https://github.com/kannahs/Lab11web/blob/master/Image%20praktikum%2013/A12.PNG?raw=true)
