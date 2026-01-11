# Jobsheet 9 – Pemrograman Jaringan: Socket Programming

### Latihan & Pengalaman Praktis

Melalui rangkaian praktikum ini, saya telah berhasil mengimplementasikan sistem komunikasi **real-time** menggunakan protokol **WebSocket** melalui library **Socket.IO**. Saya mendalami mekanisme pertukaran data dua arah (*bidirectional*) yang memungkinkan server dan klien berinteraksi secara instan tanpa ketergantungan pada siklus permintaan (*request*) HTTP konvensional.

Fokus latihan ini meliputi pengembangan aplikasi ruang obrolan (*chat room*) dengan memanfaatkan metode **event-based communication**. Saya mempelajari penggunaan `socket.on` dan `socket.emit` untuk manajemen peristiwa, pengaturan pengguna dalam grup spesifik (*rooms*), serta teknik **broadcasting** pesan agar dapat diterima oleh seluruh klien yang terhubung secara simultan.

---

### Tugas Analisis & Implementasi

#### 1. Komparasi Implementasi `socket.on` (Server vs Client)

Tabel ini membedah perbedaan peran metode `socket.on` pada infrastruktur sisi server dan antarmuka klien:

| Parameter | Sisi Server (`src/index.js`) | Sisi Klien (`public/js/chat.js`) |
| --- | --- | --- |
| **Platform** | Ekosistem Node.js | Lingkungan Browser |
| **Fungsi Utama** | Orkestrasi *event*, manajemen sesi pengguna, dan distribusi data | Resepsi *event* dari server dan pembaruan UI |
| **Event Utama** | `join`, `kirimPesan`, `kirimLokasi`, `disconnect` | `pesan`, `locationMessage`, `roomData` |
| **Tanggung Jawab** | Eksekusi logika bisnis dan validasi input | Transformasi data menjadi representasi visual |
| **Operasi Teknis** | *Broadcasting*, pembaruan status *room*, dan manajemen user | Manipulasi DOM, rendering template, dan *auto-scrolling* |
| **Output** | Transmisi *event* ke seluruh klien di *room* terkait | Modifikasi tampilan pesan dan koordinat lokasi |

---

#### 2. Investigasi Alur Data melalui Console Browser

Berdasarkan pengamatan pada konsol pengembang, berikut adalah kronologi transmisi data:

* **Pesan Sambutan Admin:** Klien menangkap objek pesan otomatis dari server saat berhasil terhubung.
* **Interaksi Pengguna:** Ketika pengguna mengirim teks, server mendistribusikan objek tersebut ke seluruh anggota *room* untuk dicetak di konsol masing-masing.
* **Konfirmasi Pengiriman:** Muncul log "Pesan berhasil dikirim" sebagai hasil dari fungsi *callback* setelah server selesai memproses emisi data.

---

#### 3. Fungsi Pustaka Eksternal pada `chat.html`

Aplikasi ini mengintegrasikan tiga library utama untuk mengoptimalkan fungsionalitas:

* **Mustache:** Bertugas sebagai mesin *templating* untuk merender elemen HTML secara dinamis menggunakan variabel seperti `{{username}}`.
* **Moment:** Digunakan untuk memproses stempel waktu (*timestamp*) mentah menjadi format waktu yang informatif (misal: jam:menit).
* **Qs:** Berfungsi membedah (*parsing*) parameter dari *query string* di URL untuk mengidentifikasi identitas pengguna dan ruangan yang dimasuki.

---

#### 4. Struktur Komponen pada `chat.js`

* **Elements:** Variabel yang menyimpan referensi ke elemen DOM (seperti tombol dan input) untuk mempermudah manipulasi skrip.
* **Templates:** Skrip yang mengambil struktur HTML dari file `chat.html` untuk digunakan oleh Mustache.
* **Options:** Objek hasil parsing URL yang mendefinisikan atribut `username` dan `room`.

---

#### 5. Modul Utilitas: `messages.js` & `users.js`

* **`messages.js`:** Berperan dalam standarisasi objek pesan (nama pengguna, teks, dan waktu) sebelum dikirimkan.
* **`users.js`:** Mengelola status keberadaan pengguna, mulai dari pendaftaran, pencarian data, hingga penghapusan saat pengguna keluar dari sistem.

---

#### 6. Mekanisme Berbagi Lokasi

Fitur ini beroperasi melalui alur berikut: browser mengakses **Geolocation API**, klien mengirimkan koordinat ke server via `socket.emit`, server mengubahnya menjadi tautan Google Maps dan melakukan **broadcast** ke ruangan, lalu klien penerima merender tautan tersebut melalui template khusus.

---

#### 7. Perbandingan Eksekusi: `npm run start` vs `npm run dev`

* **`npm run start`:** Menjalankan aplikasi secara statis melalui perintah `node`. Cocok untuk fase rilis karena lebih hemat sumber daya.
* **`npm run dev`:** Menjalankan aplikasi melalui **nodemon**, yang secara otomatis memuat ulang server setiap kali ada perubahan kode. Sangat efektif untuk fase pengembangan.

---

#### 8. Metode Operasional Socket.IO

Beberapa metode kunci yang diimplementasikan meliputi `socket.emit` (pengiriman data), `socket.broadcast.emit` (distribusi ke semua klien kecuali pengirim), `socket.join` (pengelompokan ruangan), dan `io.to().emit` (siaran spesifik ke satu ruangan).

---

#### 9. Konsep Komunikasi Real-time & Event-based

Aplikasi ini membuktikan bahwa komunikasi modern tidak lagi bersifat satu arah. Dengan pendekatan **berbasis peristiwa**, server tidak hanya menunggu tetapi dapat secara aktif mengirimkan informasi ke klien secara instan. Hal ini menciptakan pengalaman pengguna yang responsif melalui sinergi antara emisi data di sisi klien dan resepsi serta distribusi data di sisi server.

