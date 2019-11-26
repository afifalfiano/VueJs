Apa itu Vue.js ?

Singkatnya Vue.js itu merupakan sebuah Framework Javascript Progresif yang digunakan untuk membangun tampilan User Interface (UI) dengan mengacu pada arsitektur MVC (model-view-controller).

Sebelum kita belajar membuat CRUD REST API, hendaknya kita tau apa itu REST API.
RESTful API / REST API merupakan implementasi dari API (Application Programming Interface). REST (Representional State Transfer) adalah suatu arsitektur metode komunikasi yang menggunakan protokol HTTP untuk pertukaran data dan metode ini sering diterapkan dalam pengembangan aplikasi.

SET UP APLIKASI
Vue CLI akan digunakan di sini untuk mengatur aplikasi dengan cepat. Antarmuka baris perintah ini (Vue-CLI) menyediakan cara untuk cepat menghasilkan Aplikasi Halaman Tunggal dalam waktu singkat.

1. Sebelum menginstal vue-cli secara global, saya berasumsi bahwa teman-teman sudah menginstal Node dan npm, jika belum diinstall silahkan install terlebih dahulu. teman-teman dapat memverifikasi Node dan npm dari terminal (linux) atau cmd (windows) dengan:
$ node -v
$ npm -v

2. Sekarang instal Vue-CLI:
$ npm install -g vue-cli

3. Setelah menginstal CLI, perintah vue tersedia untuk perancah (scaffolding) aplikasi kita. Mari kita gunakan untuk membuat project untuk tutorial ini.
$ vue create democrud

4. Setelah membuat projectnya, lalu masuk ke direktori democrud dan lakukan instalasi
$ cd democrud
$ npm install

5. Setelah selesai, jalankan dengan perintah:
$ npm run serve
Akan muncul seperti berikut:
DONE Compiled successfully in 12870ms 10:07:35 AM
App running at:
 — Local: http://localhost:8080/ 
 — Network: http://10.100.99.97:8080/
kita pilih url localhost, lalu tampilkan di browser

6. lalu kita install Axios (untuk melakukan request HTTP) dan json-server (membuat fake REST API).
install axios :
$ npm install axios

7. install json-server dalam jangkauan global :
$ npm install -g json-server
Setelah menginstal tools yg kita perlukan, kita hapus folder components dan assets karena untuk project ini tidak diperlukan.

8. Lalu kita buat database nya di project yang tadi kita buat democrud dan buat sebuah file json, disni saya berinama dengan db.json
Untuk menampilkan apakah json nya sudah bisa diakses atau belum, ketik ini:
$ json-server db.json
Maka akan muncul seperti berikut:
\{^_^}/ hi!
Loading db.json
 Done
Resources
 http://localhost:3000/users
Home
 http://localhost:3000
Type s + enter at any time to create a snapshot of the database
Kalian pilih yang Resource, lalu tampilkan di browser

File db.json
{
  "users": [
    {
      "id": 0,
      "name": "Siswa1"
    },
    {
      "id": 1,
      "name": "Siswa2"
    },
    {
      "id": 2,
       "name": "Siswa3"
    }
  ]
}
