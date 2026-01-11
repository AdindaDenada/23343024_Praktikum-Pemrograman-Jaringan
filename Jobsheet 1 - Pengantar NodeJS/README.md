# Jobsheet 1 - Introduksi Node.js

### 1. Definisi Pemrograman Jaringan

**Pemrograman jaringan** merupakan sub-disiplin ilmu komputer yang berfokus pada pembuatan instruksi perangkat lunak agar komputer dapat saling terhubung, berinteraksi, dan bertukar data melalui infrastruktur jaringan, baik dalam skala lokal (**LAN**) maupun luas (**WAN**).

### 2. Fundamen Pemrograman Jaringan

* **Arsitektur Client-Server** → Pola komunikasi di mana satu pihak bertindak sebagai peminta layanan (klien) dan pihak lain sebagai penyedia layanan (server).

* **Protokol Jaringan** → Sekumpulan aturan standar yang mengatur jalannya komunikasi data (misalnya: HTTP, SMTP).
* **Socket** → Mekanisme ujung tombak (*endpoint*) yang digunakan aplikasi untuk mengirim atau menerima data melalui jaringan (TCP/UDP).
* **Sinkron & Asinkron** → Metode eksekusi tugas; sinkron berjalan berurutan (menunggu), sedangkan asinkron memungkinkan proses lain berjalan tanpa harus menunggu tugas sebelumnya selesai.
* **Pemrograman Web** → Pengembangan aplikasi yang dijalankan di server dan diakses oleh pengguna melalui peramban.
* **Pemrograman Mobile** → Pengembangan aplikasi seluler yang biasanya memanfaatkan REST API untuk berkomunikasi dengan basis data di server.

### 3. Kontribusi Node.js dalam Jaringan

Node.js bertindak sebagai **runtime JavaScript di sisi server** yang menerapkan model **asynchronous & event-driven**. Hal ini memberikan beberapa keuntungan:

* Efisiensi tinggi dalam menangani operasi input/output (I/O).
* Kemampuan mengelola ribuan koneksi secara simultan dengan performa stabil.
* Pemanfaatan **event loop** untuk mengeksekusi proses tanpa memblokir antrean tugas lainnya (*non-blocking*).

### 4. Keunggulan Utama Node.js

* **Skalabilitas Optimal** → Sangat handal dalam menangani beban kerja besar dengan konsumsi sumber daya yang minim.
* **Kecepatan Respons** → Menjamin performa tetap gegas meskipun menangani banyak permintaan I/O yang berat.
* **Multi-Platform** → Kompatibel untuk dijalankan pada berbagai sistem operasi seperti Windows, macOS, dan Linux.
* **Unifikasi Bahasa (Full-stack JS)** → Memungkinkan penggunaan satu bahasa pemrograman (JavaScript) untuk pengembangan sisi klien maupun server.
* **Ekosistem NPM** → Akses ke jutaan pustaka (*library*) siap pakai untuk mempercepat proses pengembangan.

---

## Kesimpulan Latihan B

* Latihan ini mendemonstrasikan proses pembuatan dan eksekusi skrip JavaScript sederhana (`hello.js`) melalui terminal.
* Hasilnya mengonfirmasi bahwa **Node.js merupakan runtime environment** yang memungkinkan JavaScript dijalankan secara mandiri di tingkat sistem/server tanpa ketergantungan pada browser.

## Kesimpulan Latihan C

* Latihan ini mempraktikkan cara membangun **server HTTP fungsional** sederhana menggunakan file `hello-world.js`.
* Server yang telah dibuat dapat diakses secara lokal melalui alamat `http://127.0.0.1:3000/`.
* Poin pentingnya adalah Node.js mempermudah pemrograman jaringan melalui modul bawaan seperti `http`, yang memungkinkan pengembang membuat server secara instan dan efisien.

---