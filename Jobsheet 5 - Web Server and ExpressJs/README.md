# Jobsheet 5 – Arsitektur Web Server & Express.js

Melalui praktikum ini, saya telah berhasil melakukan **implementasi server web menggunakan Node.js dan framework Express.js**. Materi ini memberikan pemahaman mendalam mengenai struktur dasar server, pemanfaatan framework minimalis Express untuk efisiensi pengembangan, serta penerapan **templating engine Handlebars (hbs)** guna menyajikan konten dinamis secara terstruktur.

## Eksplorasi & Implementasi Praktis

Berikut adalah ringkasan tahapan pengembangan yang telah diselesaikan secara sistematis:

1. **Fundamen Web Server** — Menganalisis mekanisme kerja server statis dibandingkan server dinamis, serta mendalami siklus interaksi antara peramban (browser) dan server melalui protokol HTTP.
2. **Routing dengan Express.js** — Menginisialisasi framework Express untuk mengelola berbagai rute aplikasi (seperti halaman utama, bantuan, dan tentang kami) menggunakan fungsi `app.get()`.
3. **Diversifikasi Respon (HTML & JSON)** — Mengintegrasikan pengiriman file HTML untuk kebutuhan antarmuka pengguna dan format data JSON untuk kebutuhan pertukaran data backend.
4. **Manajemen Aset Statis** — Mengonfigurasi direktori publik untuk file `CSS`, `JavaScript client-side`, serta aset visual menggunakan modul `path` dan middleware `express.static()`.
5. **Dinamisme dengan Handlebars (hbs)** — Mengadopsi sistem *templating* untuk menyuntikkan variabel dari sisi backend ke dalam tampilan antarmuka secara fleksibel.
6. **Optimalisasi Struktur melalui Partials** — Membangun komponen *header* dan *footer* yang dapat digunakan kembali (*reusable*) guna menjaga konsistensi desain dan mempermudah pemeliharaan kode.
7. **Visualisasi & Estetika** — Meningkatkan kualitas visual aplikasi dengan mengintegrasikan file `styles.css` dan aset ikon cuaca melalui sistem *layouting* yang rapi.
8. **Penanganan Error (Wildcard Route)** — Mengimplementasikan rute khusus menggunakan simbol wildcard untuk menangkap permintaan URL yang tidak valid dan menyajikan halaman kesalahan 404 secara dinamis.

---

## Kesimpulan

Praktikum Jobsheet 5 memberikan wawasan komprehensif mengenai **tata kelola server web modern**. Penggunaan **Express.js** terbukti mempermudah manajemen rute dan aset, sementara **Handlebars** memberikan fleksibilitas tinggi dalam pembuatan halaman yang responsif terhadap data backend. Hasil akhir dari kegiatan ini adalah sebuah aplikasi server web fungsional yang mampu menangani aset statis, menyajikan konten dinamis, serta memiliki sistem penanganan kesalahan yang profesional.