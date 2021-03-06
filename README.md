# Tixam
Aplikasi Ujian Pilihan Ganda Berbasis Komputer

## Tentang Tixam

Aplikasi ini merupakan versi kedua. Versi pertama aplikasi ini diperkenalkan dan di bagikan secara gratis pada awal tahun 2017.
Hingga saat ini masih aktif digunakan oleh beberapa sekolah di Indonesia.

## Kebutuhan Server

Aplikasi ini dibangun diatas Framework <a href="https://laravel.com/docs/5.5" target="_blank" title="silahkan buka di tab baru, dengan klik kanan atau klik CTRL + clik">Laravel 5.4</a> dan MySQL versi 5. Sebelum menjalankan aplikasi ini, silahkan disiapkan terlebih dahulu beberapa software dan ekstension berikut:

- PHP >= 7.0.0
- OpenSSL PHP Extension
- PDO PHP Extension
- Mbstring PHP Extension
- Tokenizer PHP Extension
- XML PHP Extension

Anda dapat menggunakan beberapa paket yang siap pakai untuk mempersingkat proses instalasi aplikasi ini.

## Instalasi

Disini akan saya jelaskan proses instalasi pada sistem operasi Windows.

Pertama silahkan download XAMPP, silahkan download <a href="https://www.apachefriends.org/xampp-files/7.0.32/xampp-win32-7.0.32-0-VC14-installer.exe" target="_blank" title="silahkan buka di tab baru, dengan klik kanan atau klik CTRL + clik">disini</a>.
Silahkan install XAMPP yang telah berhasil Anda download. Pastikan dikomputer Anda belum terinstall PHP & MySQL untuk menghindari konflik port. Apabila sebelumnya telah ada, silahkan cek versi PHP harus diatas 7.0.

Setelah berhasil menginstal PHP dan MySQL (dalam paket XAMPP), kita lanjutkan install composer dan gitbash.

Untuk composer silahkan download <a href="https://getcomposer.org/download/Composer-Setup.exe" target="_blank" title="silahkan buka di tab baru, dengan klik kanan atau klik CTRL + clik">disini</a>.

Untuk gitbash silahkan download <a href="https://git-scm.com/download/win" target="_blank" title="silahkan buka di tab baru, dengan klik kanan atau klik CTRL + clik">disini</a>.

Silahkan instal composer dan git bash di komputer server Anda. Setelah semua berhasil diinstal dengan benar kita bisa mulai clone aplikasi ini ke komputer kita.

Buka command promt lalu arahkan ke folder htdocs (ada didalam folder xampp, misal Anda menginstal di C. Berarti Anda harus ke folder C:\\xampp\htdocs).

Setelah itu ketikan:
```
git clone https://github.com/wisnuvb/tixam.git
```

Tunggu sampai file selesai di clone ke folder htdocs server Anda, lalu masuk ke folder <b>tixam</b> yang barusan Anda clone. Kemudian ketikan :
```
composer update --verbose --profile --prefer-dist
php artisan key:generate
```

Buka browser dan ketikan url http://localhost/phpmyadmin. Lalu buat database baru dengan nama <b>tixam</b>. Setelah itu ketikan script berikut pada command promt:
```
php artisan migrate
php artisan db:seed
```

Setelah proses diatas berhasil dilalui tanpa hambatan, silahkan akses di browser url http://localhost/tixam/public untuk mengakses aplikasi ujian.

Untuk login sebagai guru silahkan gunakan email: admin@ayosinau.com, password: secret

## Info Tambahan

Aplikasi ini bersifat terbuka, siapapun dipersilahkan untuk menjadi kontributor untuk meningkatkan kualitas aplikasi ini.

Buat yang telah berhasil menggunakan, jangan lupa untuk kasih bintang ya...
