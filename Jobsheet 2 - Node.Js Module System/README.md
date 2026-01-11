# Laporan Praktikum: Fundamental Node.js & Sistem Modul

Melalui rangkaian materi ini, saya telah mendalami implementasi sistem modularitas pada ekosistem Node.js. Fokus pembelajaran mencakup teknik enkapsulasi kode menggunakan `module.exports` dan pemanggilannya melalui `require()`, pemanfaatan modul internal seperti **File System (`fs`)**, serta manajemen pustaka pihak ketiga menggunakan **NPM (Node Package Manager)**. Selain itu, saya juga mempelajari penanganan input dinamis melalui *command line arguments* menggunakan `process.argv` dan library **yargs**.

## Rincian Implementasi Latihan

Secara sistematis, berikut adalah tahapan pengembangan yang telah diselesaikan:

1. **Manipulasi File Data:** Menggunakan modul **fs** untuk melakukan operasi dasar pada file, seperti membuat dokumen baru dan menambahkan informasi secara persisten.
2. **Modularisasi Kode Mandiri:** Membangun modul khusus (`catatan.js`) untuk memisahkan logika aplikasi, kemudian mengintegrasikannya ke skrip utama guna menciptakan struktur kode yang lebih bersih.
3. **Manajemen Ekosistem NPM:** Melakukan inisialisasi proyek melalui `npm init` serta mengelola dependensi eksternal, di antaranya:
* **validator:** Untuk memastikan integritas data input.
* **chalk:** Untuk meningkatkan *user experience* melalui pewarnaan teks di terminal.
* **nodemon:** Untuk efisiensi pengembangan dengan fitur *auto-reload* aplikasi.


4. **Interaktivitas Baris Perintah (CLI):** Mengimplementasikan parser argumen baik secara manual (`process.argv`) maupun menggunakan package **yargs** agar aplikasi dapat menerima perintah langsung dari terminal.
5. **Pengembangan Aplikasi CRUD:** Berhasil membangun aplikasi manajemen catatan berbasis terminal yang mendukung fungsi **Create, Read, Update, dan Delete**. Aplikasi ini memungkinkan pengguna untuk menambah, membaca, melihat daftar, serta menghapus data secara dinamis.