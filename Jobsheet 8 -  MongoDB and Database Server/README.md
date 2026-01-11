# Jobsheet 8 – Implementasi MongoDB & Database Server NoSQL

Melalui praktikum ini, saya telah mendalami konsep serta implementasi basis data NoSQL menggunakan **MongoDB** sebagai *database server* pada aplikasi Node.js. Fokus pembelajaran ini mencakup pemahaman mengenai dikotomi antara arsitektur relasional (SQL) dan NoSQL, terutama dalam aspek fleksibilitas skema serta efisiensi penyimpanan data berbasis dokumen (*document-based storage*).

## Eksplorasi & Capaian Praktikum

Secara bertahap, saya telah menyelesaikan serangkaian implementasi teknis berikut:

1. **Arsitektur & Integrasi Data:** Berhasil membangun koneksi antara Node.js dan MongoDB serta memahami hierarki penyimpanan yang terdiri dari *Database, Collection,* dan *Document*. Saya juga mempelajari peran **ObjectId** sebagai pengenal unik (UUID) otomatis untuk setiap entitas data.
2. **Operasi CRUD (Native Driver):** Mengimplementasikan manipulasi data secara programatik menggunakan *MongoDB Native Driver*. Operasi yang berhasil dipraktikkan meliputi:
* **Create:** Penggunaan `insertOne` dan `insertMany` untuk persistensi data.
* **Read:** Pemanfaatan fungsi `find` untuk ekstraksi data berdasarkan kriteria tertentu.
* **Update:** Implementasi `updateOne` dan `updateMany` untuk modifikasi record secara efisien.
* **Delete:** Penggunaan `deleteOne` dan `deleteMany` untuk manajemen penghapusan data.


3. **Mekanisme Asinkron & Validasi:** Memahami karakteristik interaksi database yang bersifat asinkron dalam Node.js. Selain itu, saya menggunakan **MongoDB Compass** sebagai alat bantu visual (GUI) untuk melakukan verifikasi dan pemantauan data secara *real-time*.

---

## Kesimpulan

Berdasarkan praktikum pada Jobsheet 8, dapat disimpulkan bahwa:

* **Transformasi Paradigma Data:** Pemahaman mengenai NoSQL memberikan perspektif baru dalam menangani data yang tidak terstruktur dengan skalabilitas yang lebih tinggi dibandingkan database relasional konvensional.
* **Efisiensi Backend:** Integrasi MongoDB dengan Node.js memungkinkan proses pengolahan data menjadi lebih cepat dan fleksibel, sesuai dengan tuntutan aplikasi web modern yang dinamis.
* **Kompetensi Teknis:** Saya telah menguasai alur kerja *backend* dalam mengelola siklus hidup data (CRUD) serta mampu melakukan *debugging* data melalui perangkat manajerial seperti MongoDB Compass.

Secara keseluruhan, praktikum ini memperkuat fondasi saya dalam membangun infrastruktur *backend* yang siap menangani volume data besar secara efektif dan terukur.

